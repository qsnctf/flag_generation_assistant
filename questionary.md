# Questionary - Python 交互式命令行工具库

## 概述

Questionary 是一个 Python 库，用于创建美观、交互式的命令行界面。它提供了多种类型的输入控件，让命令行程序能够以更友好的方式与用户交互。

## 主要特性

### 1. 选择菜单 (Select)
- 创建单选菜单
- 支持自定义指针样式
- 美观的界面布局

**示例代码：**
```python
import questionary

action = questionary.select(
    "请选择你要执行的操作:",
    choices=[
        "🚀 部署新版本",
        "🔍 查看系统日志",
        "🛠️ 修改配置文件",
        "📊 生成数据报告",
        "❌ 退出程序"
    ],
    pointer="👉"
).ask()
```

### 2. 多选菜单 (Checkbox)
- 允许用户选择多个选项
- 支持复选框界面
- 返回选择的列表

**示例代码：**
```python
services = questionary.checkbox(
    "选择需要部署的服务:",
    choices=["Web Server", "Database", "Redis Cache", "Auth Service"]
).ask()
```

### 3. 自动补全输入 (Autocomplete)
- 支持模糊搜索
- 忽略大小写
- 提供输入建议

**示例代码：**
```python
config_name = questionary.autocomplete(
    "请输入要编辑的配置文件名 (支持模糊搜索):",
    choices=["nginx.conf", "docker-compose.yml", "settings.py", "database.sql", "env.production"],
    ignore_case=True
).ask()
```

### 4. 其他输入类型
- **文本输入**: `questionary.text("请输入内容:").ask()`
- **密码输入**: `questionary.password("请输入密码:").ask()`
- **确认对话框**: `questionary.confirm("确定要执行吗?").ask()`
- **路径选择**: `questionary.path("请选择文件路径:").ask()`

## 安装方法

```bash
pip install questionary
```

## 在本项目中的应用

在 `main.py` 中，Questionary 被用于：

1. **主菜单导航** - 使用 `select` 方法创建程序主菜单
2. **服务部署选择** - 使用 `checkbox` 方法让用户选择要部署的服务
3. **配置文件选择** - 使用 `autocomplete` 方法提供配置文件搜索功能

## 优势

1. **用户体验友好** - 比传统的命令行参数更直观
2. **错误处理完善** - 自动验证用户输入
3. **高度可定制** - 支持自定义样式和主题
4. **跨平台兼容** - 在 Windows、macOS、Linux 上表现一致

## 与 Rich 库的配合使用

Questionary 可以与 Rich 库完美配合，创建更美观的输出：

```python
from rich.console import Console
from rich.table import Table

console = Console()

# 使用 Rich 美化输出
console.print(f"[bold green]正在部署:[/bold green] {services}...")
```

## 最佳实践

1. **提供清晰的提示信息** - 让用户明确知道需要做什么
2. **使用有意义的选项** - 选项名称应该直观易懂
3. **添加适当的验证** - 确保用户输入符合预期
4. **处理中断情况** - 使用 try-except 捕获 KeyboardInterrupt

## 相关资源

- [官方文档](https://questionary.readthedocs.io/)
- [GitHub 仓库](https://github.com/tmbo/questionary)
- [PyPI 页面](https://pypi.org/project/questionary/)

---
