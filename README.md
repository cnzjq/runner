# 代码调试工具

一款功能强大的 VS Code 插件，自动识别编程语言并在控制台输出执行结果。体积小、功能强、无依赖、零配置。

## 功能特性

- **自动语言识别**：根据文件扩展名自动识别 20+ 种编程语言
- **执行代码片段**：支持运行选中的代码片段（自动写入临时文件执行）
- **完整文件执行**：一键运行当前打开的文件
- **编译型语言支持**：自动处理编译和运行流程（Java, C, C++, Rust, Kotlin, Swift）
- **进程管理**：支持终止正在运行的代码
- **执行时间统计**：显示代码执行耗时
- **状态栏快捷按钮**：左下角显示当前可执行的语言类型
- **错误处理**：清晰的错误提示和输出信息

## 支持语言

| 语言 | 扩展名 | 执行方式 | 类型 |
|------|--------|----------|------|
| JavaScript | .js, .mjs, .cjs | node | 解释型 |
| TypeScript | .ts | node | 解释型 |
| Python | .py, .pyw, .pyi | python | 解释型 |
| PHP | .php | php | 解释型 |
| Ruby | .rb, .rbw | ruby | 解释型 |
| Go | .go | go run | 解释型 |
| Rust | .rs | rustc | 编译型 |
| Java | .java | javac + java | 编译型 |
| C | .c, .h | gcc | 编译型 |
| C++ | .cpp, .cc, .cxx, .hpp | g++ | 编译型 |
| C# | .cs | dotnet run | 编译型 |
| Shell | .sh, .bash | bash | 解释型 |
| PowerShell | .ps1, .psm1, .psd1 | powershell | 解释型 |
| Lua | .lua | lua | 解释型 |
| Perl | .pl, .pm | perl | 解释型 |
| Dart | .dart | dart | 解释型 |
| Kotlin | .kt, .kts | kotlinc | 编译型 |
| Scala | .scala, .sc | scala | 解释型 |
| Swift | .swift | swiftc | 编译型 |
| R | .r, .rmd | Rscript | 解释型 |
| Julia | .jl | julia | 解释型 |

## 快捷键

| 快捷键 | 功能 | 适用平台 |
|--------|------|----------|
| `Ctrl+Alt+N` | 运行当前文件 | Windows / Linux |
| `Cmd+Alt+N` | 运行当前文件 | macOS |
| `Ctrl+Alt+S` | 运行选中代码 | Windows / Linux |
| `Cmd+Alt+S` | 运行选中代码 | macOS |
| `Ctrl+Shift+P` | 停止运行 | Windows / Linux |

## 插件设置

打开 VS Code 设置（`Ctrl+,`），搜索 `Code Runner`：

| 设置项 | 类型 | 默认值 | 说明 |
|--------|------|--------|------|
| `codeRunnerNative.showExecutionTime` | boolean | true | 是否在输出中显示执行时间 |
| `codeRunnerNative.clearPreviousOutput` | boolean | true | 运行前是否清除之前的输出 |
| `codeRunnerNative.runInTerminal` | boolean | false | 是否在集成终端中运行代码 |

## 编译型语言执行流程

对于 Java, C, C++, Rust, Kotlin, Swift 等编译型语言，插件会自动处理编译和执行：

1. **编译阶段**：使用对应的编译器编译源代码
2. **运行阶段**：自动执行编译生成的可执行文件
3. **错误处理**：如果编译失败，会显示编译错误信息

### 各语言运行环境要求

| 语言 | 需要安装 |
|------|----------|
| JavaScript/TypeScript | Node.js |
| Python | Python 3.x |
| Java | JDK |
| C/C++ | GCC 或 Clang |
| Rust | Rust Toolchain |
| Go | Go SDK |
| 其他 | 对应语言的运行时 |

## 常见问题

### Q: 插件提示 "无法识别的文件类型" 怎么办？

A: 请确保文件有正确的扩展名。支持的扩展名见上表。如果仍有问题，请检查文件是否已保存。

### Q: 编译型语言执行失败？

A: 请确保已安装对应的编译器：
- Java: `javac` 和 `java`
- C/C++: `gcc` / `g++`
- Rust: `rustc`
- Go: `go`
- Kotlin: `kotlinc`
- Swift: `swiftc`

### Q: 执行 Python 代码时提示找不到命令？

A: 请确保 Python 已添加到系统 PATH 环境变量。在 Windows 上，命令通常为 `python` 或 `python3`。

### Q: 插件支持调试功能吗？

A: 本插件专注于代码的快速运行和结果输出，不包含调试功能。如需调试，请使用 VS Code 的内置调试功能。

## 开源协议

本项目基于 [MIT 协议](LICENSE.txt) 开源。

## 微信交流群

![微信群二维码](https://www.vipqiye.com/static/images/qun.png)
