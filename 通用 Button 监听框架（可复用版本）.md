
---

## 🎯 一、什么是委托？（3句话搞懂）

```csharp
// 委托 = 方法的"容器"或"指针"
public delegate void MyDelegate(string message);  // ① 定义：规定方法签名

MyDelegate callback = ShowMessage;  // ② 赋值：存储方法
callback("Hello");                  // ③ 调用：执行方法 → ShowMessage("Hello")

void ShowMessage(string msg) { Debug.Log(msg); }
```

**类比：** 委托 = 遥控器，可以指向不同的电视（方法），按下按钮（调用）就执行对应功能。

---

## 💻 二、通用框架代码（直接复制可用）

### **文件1：EventType.cs** (事件类型定义)

```csharp
/// <summary>
/// 通用事件类型定义
/// </summary>
public static class EventType
{
    public const string CLICK = "CLICK";
    public const string MOUSE_DOWN = "MOUSE_DOWN";
    public const string MOUSE_UP = "MOUSE_UP";
    public const string MOUSE_ENTER = "MOUSE_ENTER";
    public const string MOUSE_EXIT = "MOUSE_EXIT";
}
```

---

### **文件2：UIEventHandler.cs** (核心事件处理器)

```csharp
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.EventSystems;

/// <summary>
/// 通用UI事件处理器（支持点击、长按、悬停等）
/// </summary>
public class UIEventHandler : MonoBehaviour,
    IPointerClickHandler,
    IPointerDownHandler,
    IPointerUpHandler,
    IPointerEnterHandler,
    IPointerExitHandler
{
    // 委托定义：所有回调统一格式
    public delegate void EventCallback(GameObject sender);
    
    // 事件存储
    private EventCallback onClickEvent;
    private EventCallback onDownEvent;
    private EventCallback onUpEvent;
    private EventCallback onEnterEvent;
    private EventCallback onExitEvent;
    
    // 长按参数
    private float holdStartDelay = 0f;
    private float holdInterval = 0f;
    private float holdTimer = 0f;
    private int holdState = 0;
    
    /// <summary>
    /// 注册事件监听
    /// </summary>
    public void AddListener(string eventType, EventCallback callback, 
                           float startDelay = 0f, float interval = 0f)
    {
        switch (eventType)
        {
            case EventType.CLICK:
                onClickEvent = callback;
                // 兼容Button组件
                var btn = GetComponent<Button>();
                if (btn != null)
                    btn.onClick.AddListener(() => callback?.Invoke(gameObject));
                break;
                
            case EventType.MOUSE_DOWN:
                onDownEvent = callback;
                holdStartDelay = startDelay;
                holdInterval = interval;
                break;
                
            case EventType.MOUSE_UP:
                onUpEvent = callback;
                break;
                
            case EventType.MOUSE_ENTER:
                onEnterEvent = callback;
                break;
                
            case EventType.MOUSE_EXIT:
                onExitEvent = callback;
                break;
        }
    }
    
    // Unity事件回调
    public void OnPointerClick(PointerEventData eventData)
    {
        onClickEvent?.Invoke(gameObject);
    }
    
    public void OnPointerDown(PointerEventData eventData)
    {
        onDownEvent?.Invoke(gameObject);
        
        // 启动长按
        if (holdStartDelay > 0)
        {
            holdState = 1;
            holdTimer = Time.time;
        }
    }
    
    public void OnPointerUp(PointerEventData eventData)
    {
        onUpEvent?.Invoke(gameObject);
        holdState = 0;
    }
    
    public void OnPointerEnter(PointerEventData eventData)
    {
        onEnterEvent?.Invoke(gameObject);
    }
    
    public void OnPointerExit(PointerEventData eventData)
    {
        onExitEvent?.Invoke(gameObject);
        holdState = 0;
    }
    
    // 处理长按重复触发
    private void Update()
    {
        if (holdState == 0) return;
        
        float elapsed = Time.time - holdTimer;
        
        if (holdState == 1 && elapsed > holdStartDelay)
        {
            onDownEvent?.Invoke(gameObject);
            holdTimer = Time.time;
            holdState = holdInterval > 0 ? 2 : 0;
        }
        else if (holdState == 2 && elapsed > holdInterval)
        {
            onDownEvent?.Invoke(gameObject);
            holdTimer = Time.time;
        }
    }
}
```

---

### **文件3：UIEventManager.cs** (便捷管理类)

```csharp
using UnityEngine;
using UnityEngine.UI;

/// <summary>
/// UI事件管理器（提供便捷注册方法）
/// </summary>
public static class UIEventManager
{
    /// <summary>
    /// 为Button添加点击事件
    /// </summary>
    public static void AddClick(this Button button, UIEventHandler.EventCallback callback)
    {
        var handler = button.gameObject.GetOrAddComponent<UIEventHandler>();
        handler.AddListener(EventType.CLICK, callback);
    }
    
    /// <summary>
    /// 为GameObject添加长按事件
    /// </summary>
    public static void AddLongPress(this GameObject obj, UIEventHandler.EventCallback callback,
                                   float startDelay = 0.5f, float interval = 0.1f)
    {
        var handler = obj.GetOrAddComponent<UIEventHandler>();
        handler.AddListener(EventType.MOUSE_DOWN, callback, startDelay, interval);
    }
    
    /// <summary>
    /// 为GameObject添加悬停事件
    /// </summary>
    public static void AddHover(this GameObject obj, 
                               UIEventHandler.EventCallback onEnter,
                               UIEventHandler.EventCallback onExit)
    {
        var handler = obj.GetOrAddComponent<UIEventHandler>();
        handler.AddListener(EventType.MOUSE_ENTER, onEnter);
        handler.AddListener(EventType.MOUSE_EXIT, onExit);
    }
    
    /// <summary>
    /// 获取或添加组件
    /// </summary>
    private static T GetOrAddComponent<T>(this GameObject obj) where T : Component
    {
        var component = obj.GetComponent<T>();
        return component != null ? component : obj.AddComponent<T>();
    }
}
```

---

## 🚀 三、使用示例

### **示例1：统一回调方式**

```csharp
public class GameController : MonoBehaviour
{
    void Start()
    {
        // 批量注册
        RegisterButton("Button_Start");
        RegisterButton("Button_Pause");
        RegisterButton("Button_Quit");
    }
    
    void RegisterButton(string buttonName)
    {
        var btn = GameObject.Find(buttonName).GetComponent<Button>();
        var handler = btn.gameObject.AddComponent<UIEventHandler>();
        handler.AddListener(EventType.CLICK, OnButtonClick);
    }
    
    // 统一回调
    void OnButtonClick(GameObject obj)
    {
        switch (obj.name)
        {
            case "Button_Start":
                StartGame();
                break;
            case "Button_Pause":
                PauseGame();
                break;
            case "Button_Quit":
                QuitGame();
                break;
        }
    }
}
```

---

### **示例2：扩展方法使用（推荐）**

```csharp
public class SimpleController : MonoBehaviour
{
    public Button btnStart;
    public Button btnAddScore;
    public GameObject tooltip;
    
    void Start()
    {
        // 普通点击
        btnStart.AddClick(obj => StartGame());
        
        // 长按加分（0.5秒后开始，每0.1秒加100分）
        btnAddScore.AddLongPress(obj => AddScore(100), 0.5f, 0.1f);
        
        // 悬停显示提示
        tooltip.AddHover(
            onEnter: obj => obj.SetActive(true),
            onExit: obj => obj.SetActive(false)
        );
    }
    
    void StartGame() { Debug.Log("游戏开始"); }
    void AddScore(int score) { Debug.Log($"加分：{score}"); }
}
```

---

### **示例3：Lambda表达式**

```csharp
// 简洁写法
btnStart.AddClick(obj => Debug.Log("开始"));
btnPause.AddClick(obj => Time.timeScale = 0);
btnResume.AddClick(obj => Time.timeScale = 1);
```

---

## 🔑 四、核心优势

| 特性 | 说明 |
|------|------|
| **✅ 零依赖** | 只依赖 Unity 原生 API |
| **✅ 开箱即用** | 复制3个文件即可使用 |
| **✅ 支持长按** | 内置长按重复触发 |
| **✅ 扩展方法** | 链式调用更简洁 |
| **✅ 统一回调** | 支持集中管理 |

---

## 📝 五、快速上手（3步）

```csharp
// 步骤1：复制上面3个文件到项目

// 步骤2：使用扩展方法（推荐）
btnStart.AddClick(obj => StartGame());

// 或步骤2：手动注册
var handler = btnStart.gameObject.AddComponent<UIEventHandler>();
handler.AddListener(EventType.CLICK, OnClick);

// 步骤3：实现回调
void OnClick(GameObject obj)
{
    Debug.Log($"点击了：{obj.name}");
}
```

---

## 💡 六、委托理解（记忆版）

```csharp
// 委托 = 方法的变量
delegate void MyDelegate(int x);  // 定义：方法必须是 void(int)

MyDelegate d;           // 声明：创建容器
d = Method1;            // 赋值：存储方法
d(100);                 // 调用：Method1(100)

void Method1(int x) { }
```

**3个关键词：**
1. **定义**：规定方法签名
2. **赋值**：存储方法引用
3. **调用**：执行方法

**实际作用：** 让方法像变量一样传递，实现**回调机制**。

---

**搞定！复制这3个文件就能在任何Unity项目中使用了！** 🎉