# c++编译-launch.json

{

    // 使用 IntelliSense 了解相关属性。

    // 悬停以查看现有属性的描述。

    // 欲了解更多信息，请访问: [https://go.microsoft.com/fwlink/?linkid=830387](https://go.microsoft.com/fwlink/?linkid=830387)

    "version": "0.2.0",

    "configurations": [

        {

            "preLaunchTask": "Makefile生成可执行文件",

            "name": "(gdb) 启动",

            "type": "cppdbg",

            "request": "launch",

            "program": "${workspaceRoot}/pa0/build/Transformation.exe",

            "args": [],

            "stopAtEntry": false,

            "cwd": "${fileDirname}",

            "environment": [],

            "externalConsole": false,

            "MIMode": "gdb",

            "miDebuggerPath": "C:/Users/25365/libs/mingw64/bin/gdb.exe",

            "setupCommands": [

                {

                    "description": "为 gdb 启用整齐打印",

                    "text": "-enable-pretty-printing",

                    "ignoreFailures": true

                },

                {

                    "description": "将反汇编风格设置为 Intel",

                    "text": "-gdb-set disassembly-flavor intel",

                    "ignoreFailures": true

                }

            ]

        }

       

    ]

}

---

这是一个 Visual Studio Code (VSCode) 的调试配置文件，用于通过 GDB (GNU Debugger) 调试 C++ 项目。以下是配置文件的主要部分解释：

- `"version": "0.2.0"`: 表示调试配置文件的版本。

- `"configurations": [...]`: 包含一个调试配置的数组。

  - **第一个配置:**

    - `"preLaunchTask": "Makefile生成可执行文件"`: 在启动调试器之前运行的任务，确保 Makefile 已生成并且可执行文件已构建。

    - `"name": "(gdb) 启动"`: 调试配置的名称。

    - `"type": "cppdbg"`: 指定调试器类型为 C/C++ 调试器。

    - `"request": "launch"`: 表示启动调试器。

    - `"program": "${workspaceRoot}/pa0/build/Transformation.exe"`: 要调试的可执行文件的路径。

    - `"args": []`: 启动可执行文件时传递的命令行参数。

    - `"stopAtEntry": false`: 是否在程序的入口处停止。

    - `"cwd": "${fileDirname}"`: 设置当前工作目录为当前打开文件的目录。

    - `"environment": []`: 设置环境变量。

    - `"externalConsole": false`: 是否使用外部控制台。

    - `"MIMode": "gdb"`: 使用 GDB 模式进行调试。

    - `"miDebuggerPath": "C:/Users/25365/libs/mingw64/bin/gdb.exe"`: GDB 可执行文件的路径。

    - `"setupCommands": [...]`: 用于设置 GDB 的一系列命令，包括启用漂亮打印和将反汇编风格设置为 Intel。

这个调试配置的目的是使用 GDB 调试生成的可执行文件，确保构建任务 "Makefile生成可执行文件" 在调试开始之前运行。调试器配置还包含一些 GDB 的启动设置，以确保更好的调试体验。可以通过 VSCode 中的调试器功能执行此调试配置。
