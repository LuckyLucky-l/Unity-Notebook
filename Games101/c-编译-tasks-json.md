# c++编译-tasks.json

1.tasks.json:

{

    "tasks": [

        {

            "type": "cppbuild",

            "label": "C/C++: g++.exe 生成活动文件",

            "command": "C:\\Users\\25365\\libs\\mingw64\\bin\\g++.exe",

            "args": [

                "-fdiagnostics-color=always",

                "-g",

                "${file}",

                "-o",

                "${fileDirname}\\${fileBasenameNoExtension}.exe"

            ],

            "options": {

                "cwd": "${fileDirname}"

            },

            "problemMatcher": [

                "$gcc"

            ],

            "group": {

                "kind": "build",

                "isDefault": true

            },

            "detail": "调试器生成的任务。"

        },

        {

            "type": "cppbuild",

            "label": "cmake生成Makefile",

            "command": "cmake.exe",

            "args": [

                "-B",

                "build",

                "-G",

                "MinGW Makefiles"

            ],

            "options": {

                "cwd": "${fileDirname}"

            },

            "problemMatcher": [

                "$gcc"

            ],

            "group": {

                "kind": "build",

                "isDefault": true

            },

            "detail": "调试器生成的任务。"

        },

        {

            "dependsOn":["cmake生成Makefile"],

            "type": "cppbuild",

            "label": "Makefile生成可执行文件",

            "command": "mingw32-make.exe",

            "args": [

            "-C",

            "build"

            ],

            "options": {

                "cwd": "${fileDirname}"

            },

            "problemMatcher": [

                "$gcc"

            ],

            "group": {

                "kind": "build",

                "isDefault": true

            },

            "detail": "调试器生成的任务。"

        }

    ],

    "version": "2.0.0"

}

---

这是一个在 Visual Studio Code (VSCode) 中配置的 C/C++ 构建任务序列，用于使用 CMake 和 MinGW 编译器生成和构建项目。让我逐一解释这些任务的作用：

1. **"C/C++: g++.exe 生成活动文件"**

   - **类型 (`type`):** cppbuild

   - **标签 (`label`):** C/C++: g++.exe 生成活动文件

   - **命令 (`command`):** g++ 编译器的可执行文件路径

   - **参数 (`args`):** 包括启用彩色诊断、生成调试信息、输入文件路径、输出文件路径等参数

   - **选项 (`options`):** 当前工作目录设置为文件的目录

   - **问题匹配器 (`problemMatcher`):** 使用 $gcc 匹配器，用于在输出中识别编译错误和警告

   - **分组 (`group`):** 设置为默认构建任务，并分组为构建任务

   - **详细信息 (`detail`):** 提供关于任务的详细信息，表示这是调试器生成的任务

2. **"cmake生成Makefile"**

   - **类型 (`type`):** cppbuild

   - **标签 (`label`):** cmake生成Makefile

   - **命令 (`command`):** cmake.exe

   - **参数 (`args`):** 包括设置构建目录、选择生成器等参数

   - **选项 (`options`):** 当前工作目录设置为文件的目录

   - **问题匹配器 (`problemMatcher`):** 使用 $gcc 匹配器

   - **分组 (`group`):** 设置为默认构建任务，并分组为构建任务

   - **详细信息 (`detail`):** 提供关于任务的详细信息，表示这是调试器生成的任务

3. **"Makefile生成可执行文件"**

   - **依赖 (`dependsOn`):** 依赖于前一个任务 "cmake生成Makefile"

   - **类型 (`type`):** cppbuild

   - **标签 (`label`):** Makefile生成可执行文件

   - **命令 (`command`):** mingw32-make.exe

   - **参数 (`args`):** 包括设置构建目录

   - **选项 (`options`):** 当前工作目录设置为文件的目录

   - **问题匹配器 (`problemMatcher`):** 使用 $gcc 匹配器

   - **分组 (`group`):** 设置为默认构建任务，并分组为构建任务

   - **详细信息 (`detail`):** 提供关于任务的详细信息，表示这是调试器生成的任务

这个任务序列的目的是通过 CMake 生成 Makefile，并使用 Makefile 编译和构建项目。每个任务都有特定的目的，而第三个任务依赖于第二个任务，确保在构建可执行文件之前先生成了 Makefile。可以通过 VSCode 的构建系统执行这些任务。
