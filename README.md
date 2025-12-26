# 青少年CTF工具模板 (QSNCTF Tools Template)

一个基于 Python 的命令行工具模板。该项目展示了如何使用现代化的命令行界面库来构建交互式工具。

## 🚀 项目特色

- **美观的交互界面** - 使用 Questionary 库提供友好的命令行交互体验
- **彩色输出** - 集成 Rich 库实现彩色和格式化输出
- **模块化设计** - 采用模块化架构，便于扩展和维护
- **青少年CTF专用** - 专为青少年网络安全爱好者设计

## 📁 项目结构

```
qsnctf_tools_template/
├── main.py                 # 主程序入口
├── config.yml              # 配置文件
├── questionary.md          # Questionary 库使用文档
├── README.md               # 项目说明文档
└── module/                 # 模块目录
    ├── qsnctf_welcome/     # 欢迎模块
    │   └── __init__.py
    └── qsnctf_progress/    # 进度条模块
        └── __init__.py
```

## 🛠️ 功能特性

### 1. 主菜单系统
- 使用 Questionary 的选择菜单
- 支持自定义指针样式
- 提供多种操作选项

### 2. 服务部署功能
- 多选菜单选择部署服务
- 支持 Web Server、Database、Redis Cache、Auth Service 等

### 3. 配置文件管理
- 自动补全输入支持模糊搜索
- 配置文件快速选择

### 4. 数据报告生成
- 集成 Rich 表格显示
- 美观的系统状态展示

## 📦 依赖库

- **questionary** - 交互式命令行界面
- **rich** - 终端美化输出
- **pyyaml** - YAML 配置文件解析

## 🚀 快速开始

### 安装依赖

```bash
pip install questionary rich pyyaml
```

### 运行程序

```bash
python main.py
```

## 💡 使用示例

运行程序后，您将看到：

1. **彩虹色的欢迎界面** - 显示项目标题和版本信息
2. **主菜单选择** - 提供以下选项：
   - 🚀 部署新版本
   - 🔍 查看系统日志
   - 🛠️ 修改配置文件
   - 📊 生成数据报告
   - ❌ 退出程序

### 部署新版本示例

选择"🚀 部署新版本"后：
- 使用复选框选择要部署的服务
- 程序会显示选中的服务列表
- 使用彩色进度条显示部署进度

### 配置文件管理示例

选择"🛠️ 修改配置文件"后：
- 使用自动补全功能搜索配置文件
- 支持模糊匹配和忽略大小写
- 快速定位目标配置文件

## 🔧 模块说明

### qsnctf_welcome 模块

提供欢迎界面功能：
- 彩虹色 ASCII 艺术显示
- 配置信息读取和显示
- 字符渐变效果

### qsnctf_progress 模块

提供进度条功能：
- 彩色旋转动画
- 百分比显示
- 自定义宽度设置

## ⚙️ 配置说明

编辑 `config.yml` 文件来自定义项目设置：

```yaml
title: 青少年CTF工具示例
version: 1.0.0
```

## 🎯 开发指南

### 添加新功能模块

1. 在 `module/` 目录下创建新模块
2. 实现模块功能
3. 在 `main.py` 中导入和使用

### 自定义界面样式

- 修改 Questionary 的 `pointer` 参数来自定义指针样式
- 使用 Rich 的样式标记来美化输出
- 调整颜色方案以适应不同主题

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request 来改进这个项目！

## 📄 许可证

本项目仅供学习和教育用途。

## 🔗 相关资源

- [Questionary 文档](https://questionary.readthedocs.io/)
- [Rich 库文档](https://rich.readthedocs.io/)
- [青少年CTF官方网站](https://www.qsnctf.com/)

---

# emoji参考

https://cn.piliapp.com/emoji/list/#tag

*让命令行工具开发变得更加有趣和高效！*