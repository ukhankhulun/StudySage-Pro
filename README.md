StudySage Pro（智学题库专家）- 多学科学习资料自动爬取与智能整理系统
---

---
📚 项目简介 | Project Introduction
StudySage Pro（智学题库专家）—— 一款专为学习者打造的「多学科资料自动化神器」，基于 Python 开发，兼顾 实用性、易用性与技术练手价值。
无需复杂操作，通过简洁的图形化界面（GUI），即可自动爬取、分类、整理各类学习资料，覆盖高考各科、雅思、小语种、学科竞赛等全场景，彻底解放手动整理资料的时间，让你专注于学习本身。
同时，作为 Python 实战项目，完美适配 AI 专业学习与 GitHub 作品集展示，新手可快速上手，进阶者可拓展功能，实现「学习+技术」双向提升。
Core Goal: Free up time for manual data organization, focus on learning itself, and serve as a practical Python project for AI major learning and GitHub portfolio display.
🖼️ 界面预览 | Interface Preview
> 建议补充项目GUI截图（可上传至仓库assets文件夹，替换下方链接），提升视觉吸引力

Tip: 截图建议包含主界面、爬取进度页、导出结果页，让用户直观了解项目功能。
🚀 核心功能 | Core Features
功能模块 | Module
核心能力 | Core Capabilities
适用场景 | Application Scenario
🌐 多学科资料爬取
支持高考各科、雅思、小语种、竞赛资料，可扩展自定义数据源
学生备考、资料收集、知识点汇总
🖥️ 图形化操作界面
无需命令行，点击操作，实时显示进度、异常提示清晰
新手操作、快速上手、高效使用
📊 智能整理导出
自动拆分题型、提取知识点/词汇/公式，支持Excel/Word/PDF导出
题库整理、打印背诵、错题归档
🔧 实用拓展功能
断点续爬、自动去重、日志记录、数据源切换
高效爬取、问题排查、灵活适配
🤖 AI 可扩展
对接大模型、双语翻译、本地知识库，贴合AI专业学习
知识点解析、多语言学习、智能检索
📋 环境要求 | Environment Requirements
确保本地环境满足以下要求，避免运行异常（版本可兼容更高版本）：
环境/工具 | Environment/Tool
版本要求 | Version Requirement
说明 | Description
Python
3.8+
核心运行环境，建议使用3.9版本（兼容性最佳）
PyQt5
5.15+
图形化界面开发核心框架，负责界面渲染与交互
Scrapy
2.8+
爬虫核心框架，实现多源资料自动爬取
openpyxl
3.1+
Excel文件生成与编辑，用于题库导出
python-docx
0.8+
Word文件生成，支持知识点/词汇手册导出
pdfplumber
0.10+
PDF内容提取（可选），用于解析PDF格式资料
requests
2.31+
网络请求工具，获取网页数据
beautifulsoup4
4.12+
网页解析工具，提取有效学习资料
⚙️ 安装步骤 | Installation Steps
全程简单操作，新手可直接复制命令执行，无需额外配置：
1. 克隆仓库（本地运行）
# 克隆仓库到本地
git clone https://github.com/ukhankhulun/StudySage-Pro.git

# 进入项目目录
cd StudySage-Pro
2. 安装依赖（一键执行）
# Windows系统
pip install -r requirements.txt

# Mac/Linux系统
pip3 install -r requirements.txt
Tip: 若安装失败，可尝试升级pip后重新安装：pip install --upgrade pip
3. 启动程序（图形化界面）
# Windows系统
python main.py

# Mac/Linux系统
python3 main.py
✅ 运行后将自动弹出图形化界面，无需额外配置，直接点击操作即可。
After running, the GUI will pop up automatically, no additional configuration is required, and you can operate directly by clicking.
📖 使用说明 | User Guide
图形化界面操作简单，全程点击即可完成，步骤如下：
1. 启动程序：运行main.py，弹出主界面，左侧显示支持的学科列表（高考各科、雅思、小语种等）。
2. 选择参数：
        
  - 勾选需要爬取的学科（可多选，如“高考英语”“高考数学”“雅思真题”）
  - 选择年份范围（如 2020-2025 年，可自定义调整）
  - 选择资料类型（真题/模拟题/词汇/公式，可多选）
  - 设置保存路径（默认保存在 output 文件夹，可自定义修改）
3. 开始爬取：点击「开始爬取」按钮，右侧日志区实时显示爬取进度、成功条数、异常提示。
4. 导出资料：爬取完成后，点击「导出文件」，选择导出格式（Excel/Word），系统自动生成标准化文件，保存至设置路径。
5. 拓展操作：
        
  - 点击「设置」：可添加自定义数据源、修改爬取频率、清除日志
  - 点击「错题管理」：可标记错题、生成错题本、导出错题解析
  - 点击「词汇/公式」：可单独导出爬取的高频词汇、学科公式，方便打印背诵
📂 项目目录结构 | Directory Structure
StudySage-Pro/
├── main.py                  # 主程序入口（启动GUI界面）
├── requirements.txt         # 依赖库清单（一键安装）
├── README.md                # 项目说明文档（本文档）
├── LICENSE                  # 开源许可证（MIT）
├── assets/                  # 静态资源文件夹（存放截图、图标等）
├── src/                     # 核心代码目录（模块化设计，易扩展）
│   ├── gui/                 # 图形化界面模块（PyQt5）
│   │   ├── main_window.py   # 主窗口设计（界面布局、按钮绑定）
│   │   └── widgets.py       # 自定义组件（进度条、日志框、复选框等）
│   ├── crawler/             # 爬虫模块（多源资料爬取）
│   │   ├── base_crawler.py  # 基础爬虫类（统一接口，便于扩展）
│   │   ├── gaokao/          # 高考各科爬虫（英语/数学/理化等）
│   │   ├── ielts/           # 雅思资料爬虫（真题/词汇/听力）
│   │   └── minor_language/  # 小语种爬虫（蒙语/日语/韩语等）
│   ├── processor/           # 资料处理模块（数据清洗与导出）
│   │   ├── data_clean.py    # 数据去重、清洗、题型拆分
│   │   ├── excel_export.py  # Excel文件生成与导出
│   │   └── word_export.py   # Word文件生成与导出
│   └── utils/               # 工具函数模块（通用功能）
│       ├── log.py           # 日志记录（实时输出、文件保存）
│       └── config.py        # 配置文件（保存用户设置、数据源地址）
└── output/                  # 输出文件夹（自动生成，存放爬取的资料）
模块化设计：各模块独立运行，可单独修改、扩展，降低维护成本，适合新手学习与进阶开发。
❓ 常见问题 | FAQ
遇到问题先查看以下常见解决方案，若仍无法解决，可联系作者反馈。
1. 爬取失败怎么办？
  - 检查网络连接，确保目标网站可正常访问
  - 查看日志区提示，若显示“数据源不可用”，可在「设置」中切换数据源
  - 确认 Python 版本和依赖库版本符合要求，重新安装依赖
2. 可以添加自定义学科/数据源吗？
  - 可以！在 src/crawler/ 目录下新建爬虫类，继承 base_crawler.py 中的基础类，配置数据源地址即可
  - 详细扩展教程见「贡献说明」
3. 图形化界面无法启动？
  - 检查 PyQt5 是否安装成功，可重新执行 pip install PyQt5
  - 若仍有问题，尝试使用 Python 3.9 版本（兼容性最佳）
  - Windows系统若提示“缺少.dll文件”，可安装 Microsoft Visual C++ Redistributable
4. 资料导出后格式错乱？
  - 确保 openpyxl、python-docx 版本符合要求
  - 避免中文路径，保存路径建议使用英文/数字命名
  - 导出时关闭已打开的Excel/Word文件，避免文件占用
5. 如何中断爬取？
  - 点击界面「停止爬取」按钮，系统会保存已爬取的内容，再次启动可断点续爬
📈 升级计划 | Upgrade Plan
持续优化功能，贴合 AI 专业学习与用户实际需求，后续将逐步实现以下功能：
1. 新增 AI 真题解析功能（对接 LangChain + 开源大模型，实现题目解析、知识点推荐）
2. 优化 GUI 界面，增加主题切换（浅色/深色模式）、数据可视化（题型分布、高频词汇统计）
3. 新增学习计划功能，自动根据爬取的资料生成个性化刷题计划
4. 优化爬虫效率，增加多线程爬取，支持更多数据源
🤝 贡献指南 | Contribution Guidelines
欢迎所有形式的贡献！无论是提Bug、提需求，还是提交代码PR，都能帮助项目变得更好，新手也可参与～
1. Fork 本仓库（点击GitHub仓库右上角「Fork」按钮）
2. 创建特性分支：git checkout -b feature/AmazingFeature
3. 提交修改：git commit -m 'Add some AmazingFeature'（说明修改内容）
4. 推送分支：git push origin feature/AmazingFeature
5. 打开 Pull Request（在GitHub仓库中提交PR，详细说明修改内容）
提交PR前，请确保代码规范，添加相关测试用例，避免语法错误；若有新增功能，需补充对应的使用说明。
📄 许可证 | License
本项目基于MIT License 开源，允许自由使用、修改和分发，前提是遵循许可证协议。
Note: 本项目仅用于学习交流，爬取的资料仅用于个人学习，请勿用于商业用途，尊重版权。
🙏 致谢 | Acknowledgements
- 感谢 Scrapy、PyQt5、openpyxl 等开源库提供的技术支持
- 感谢所有为项目提建议、贡献代码的开发者
- 感谢每一位使用、Star 本项目的用户，你们的支持是项目持续优化的动力！
👨‍💻 作者信息 | Author Information
- GitHub: ukhankhulun
- 邮箱: khankhulun@outlook.com
- 说明：若有问题、建议或合作意向，可通过上述方式联系我，看到会及时回复～
---
✨ StudySage Pro - 让学习更高效，让成长更轻松 ✨
Star 🌟 不迷路，持续更新中...
