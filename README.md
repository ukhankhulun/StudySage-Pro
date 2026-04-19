StudySage Pro（智学题库专家）- 多学科学习资料自动爬取与智能整理系统
![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)
![Stars](https://img.shields.io/github/stars/ukhankhulun/StudySage-Pro)
![License](https://img.shields.io/github/license/ukhankhulun/StudySage-Pro)
项目介绍（Project Introduction）
StudySage Pro（智学题库专家）是一款基于 Python 开发的 多学科学习资料自动化工具，专为学生（尤其是高中生）打造，支持自动爬取、分类、整理各类学习资料，涵盖高考各科、雅思、小语种、竞赛等，搭配简洁图形化界面（GUI），无需命令行操作，新手也能快速上手。
核心目标（Core Goal）：解放手动整理资料的时间，专注学习本身，同时作为 Python 实战项目，适配 AI 专业学习、GitHub 作品集展示，兼顾实用性与技术练手价值。
核心功能（Core Features）
🌐 多学科资料爬取（支持扩展）
- 高考类：英语、数学、物理、化学、生物、地理、历史、政治（历年真题、模拟题、知识点汇总）
- 语言类：雅思（真题、听力原文、词汇）、小语种（日语、韩语、蒙语等基础词汇+真题）
- 拓展类：学科竞赛题、知识点速记手册、公式/词汇汇总
🖥️ 简洁图形化界面（GUI）
- 无需命令行，点击操作即可完成爬取、导出、设置
- 支持选择学科、年份、资料类型（真题/模拟题/词汇）
- 实时显示爬取进度、日志，异常提示清晰
- 自定义保存路径、导出格式（Excel/Word/PDF）
📊 智能整理与导出
- 自动拆分题型（选择题、填空题、阅读题、作文等）
- 提取核心知识点、高频词汇、公式（数学/物理/化学）
- 生成标准化题库（Excel 分工作表，含年份、题型、题目、答案、解析）
- 支持错题标记、词汇/公式单独导出（方便打印背诵）
🔧 实用拓展功能
- 断点续爬：中途停止后，再次运行可继续爬取未完成内容
- 数据源切换：支持自定义添加资料网站，适配不同地区真题
- 自动去重：避免重复爬取同一资料，节省存储空间
- 日志记录：保存爬取历史，方便追溯与排查问题
🚀 可扩展方向（贴合 AI 专业学习）
- 对接 AI 大模型：实现真题解析、错题分析、知识点推荐
- 多语言翻译：蒙汉/英汉/日汉等双语对照（适配小语种学习）
- 本地知识库：搭建个人学习资料检索系统
- 定时爬取：自动更新最新真题、考试资讯
环境要求（Environment Requirements）
环境/工具（Environment/Tool）
版本要求（Version Requirement）
说明（Description）
Python
3.8+
核心运行环境（Core Runtime Environment）
PyQt5
5.15+
图形化界面开发（GUI Development）
Scrapy
2.8+
爬虫核心框架（Core Crawler Framework）
openpyxl
3.1+
Excel 文件生成与编辑（Excel Generation & Editing）
python-docx
0.8+
Word 文件生成（Word Generation）
pdfplumber
0.10+
PDF 内容提取（可选，PDF Content Extraction (Optional)）
requests
2.31+
网络请求（Network Requests）
beautifulsoup4
4.12+
网页解析（Web Page Parsing）
安装步骤（Installation Steps）
1. 克隆仓库（本地运行）
git clone https://github.com/ukhankhulun/StudySage-Pro.git
cd StudySage-Pro
2. 安装依赖（一键执行）
# Windows
pip install -r requirements.txt

# Mac/Linux
pip3 install -r requirements.txt
3. 运行程序（图形化界面）
# Windows
python main.py

# Mac/Linux
python3 main.py
> 运行后将自动弹出图形化界面，无需额外配置，直接操作即可。（After running, the GUI will pop up automatically, no additional configuration is required, and you can operate directly.）
使用说明（GUI 操作步骤）
1. 启动程序：运行 main.py，弹出主界面，显示支持的学科列表（Launch the program: Run main.py, the main interface will pop up, showing the list of supported subjects）
2. 选择参数：
        
  - 勾选需要爬取的学科（可多选，如“高考英语”“高考数学”“雅思真题”）（Check the subjects to be crawled (multiple choices allowed, such as "Gaokao English", "Gaokao Mathematics", "IELTS Real Questions")）
  - 选择年份范围（如 2020-2025 年）（Select the year range (e.g., 2020-2025)）
  - 选择资料类型（真题/模拟题/词汇/公式）（Select the data type (real questions/simulation questions/vocabulary/formulas)）
  - 设置保存路径（默认保存在 output 文件夹）（Set the save path (default saved in the output folder)）
3. 开始爬取：点击「开始爬取」按钮，实时查看爬取进度（日志区显示）（Start crawling: Click the "Start Crawling" button to view the crawling progress in real time (displayed in the log area)）
4. 导出资料：爬取完成后，点击「导出文件」，选择导出格式（Excel/Word），自动生成标准化文件（Export data: After crawling, click "Export File", select the export format (Excel/Word), and the standardized file will be generated automatically）
5. 拓展操作：
       
  - 点击「设置」，可添加自定义数据源、修改爬取频率（Click "Settings" to add custom data sources and modify crawling frequency）
  - 点击「错题管理」，可标记错题、生成错题本（Click "Error Question Management" to mark error questions and generate error question books）
项目目录结构（Project Directory Structure）
StudySage-Pro/
├── main.py                  # 主程序（启动GUI界面）
├── requirements.txt         # 依赖库清单
├── README.md                # 项目说明（本文档）
├── LICENSE                  # 开源许可证
├── src/                     # 核心代码目录
│   ├── gui/                 # 图形化界面模块（PyQt5）
│   │   ├── main_window.py   # 主窗口设计
│   │   └── widgets.py       # 自定义组件（按钮、进度条等）
│   ├── crawler/             # 爬虫模块
│   │   ├── base_crawler.py  # 基础爬虫类（统一接口）
│   │   ├── gaokao/          # 高考各科爬虫（英语/数学/理化等）
│   │   ├── ielts/           # 雅思资料爬虫
│   │   └── minor_language/  # 小语种资料爬虫
│   ├── processor/           # 资料处理模块
│   │   ├── data_clean.py    # 数据去重、清洗
│   │   ├── excel_export.py  # Excel 导出
│   │   └── word_export.py   # Word 导出
│   └── utils/               # 工具函数
│       ├── log.py           # 日志记录
│       └── config.py        # 配置文件
└── output/                  # 输出文件夹（自动生成，存放爬取的资料）
常见问题（FAQ）
1. 爬取失败怎么办？（What if crawling fails?）
  - 检查网络连接，确保目标网站可访问（Check the network connection to ensure the target website is accessible）
  - 查看日志区提示，若提示“数据源不可用”，可在「设置」中切换数据源（Check the prompt in the log area; if it prompts "data source unavailable", you can switch the data source in "Settings"）
  - 确认 Python 版本和依赖库版本符合要求（Ensure that the Python version and dependency library versions meet the requirements）
2. 可以添加自定义学科/数据源吗？（Can I add custom subjects/data sources?）
  - 可以！在 src/crawler/ 目录下新建爬虫类，继承 base_crawler.py 中的基础类，配置数据源地址即可（Yes! Create a new crawler class in the src/crawler/ directory, inherit the base class in base_crawler.py, and configure the data source address）
  - 详细扩展教程见「贡献说明」（See "Contribution Guidelines" for detailed expansion tutorials）
3. 图形化界面无法启动？（What if the GUI fails to start?）
  - 检查 PyQt5 是否安装成功，可重新执行 pip install PyQt5（Check if PyQt5 is installed successfully; you can re-execute pip install PyQt5）
  - 若仍有问题，尝试使用 Python 3.9 版本（兼容性最佳）（If the problem persists, try using Python 3.9 (best compatibility)）
4. 资料导出后格式错乱？（What if the format is messed up after exporting data?）
  - 确保 openpyxl、python-docx 版本符合要求（Ensure that the versions of openpyxl and python-docx meet the requirements）
  - 避免中文路径，保存路径建议使用英文/数字命名（Avoid Chinese paths; it is recommended to use English/numbers for the save path）
升级计划（Upgrade Plan）（贴合 AI 专业学习）
1. 新增 AI 真题解析功能（对接 LangChain + 开源大模型）（Add AI real question analysis function (connect to LangChain + open source large model)）
2. 优化 GUI 界面，增加主题切换、数据可视化（题型分布、高频词汇统计）（Optimize the GUI interface, add theme switching and data visualization (question type distribution, high-frequency vocabulary statistics)）
3. 支持手机端访问（搭建简易 Web 服务，基于 FastAPI）（Support mobile access (build a simple Web service based on FastAPI)）
4. 新增学习计划功能，自动根据爬取的资料生成刷题计划（Add a study plan function to automatically generate a question brushing plan based on the crawled data）
贡献说明（Contribution Guidelines）
欢迎 Fork 本仓库，提交 PR 完善功能：（Welcome to Fork this repository and submit PR to improve the function:）
- 新增学科爬虫（如竞赛资料、更多小语种）（Add new subject crawlers (such as competition materials, more minor languages)）
- 优化 GUI 界面体验（Optimize GUI experience）
- 修复 bug、完善文档（Fix bugs and improve documentation）
- 新增实用功能（如 AI 分析、多端同步）（Add practical functions (such as AI analysis, multi-terminal synchronization)）
提交 PR 前，请确保代码规范，添加相关测试用例，详细说明修改内容。（Before submitting a PR, please ensure that the code is standardized, add relevant test cases, and detailedly explain the modified content.）
许可证（License）
MIT License
作者信息（Author Information）
- GitHub: ukhankhulun
- 邮箱: khankhulun@outlook.com
- 说明：本项目仅用于学习交流，爬取的资料仅用于个人学习，请勿用于商业用途，尊重版权。（Note: This project is for learning and exchange only. The crawled data is for personal learning only, please do not use it for commercial purposes and respect copyright.）
