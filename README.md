<p align="center"><img src="assets/logo.png" width="300" alt="KNX FlowGen"></p>

# KNX FlowGen 2.0

**规划更清晰，交付更从容。**

面向 KNX 工程师、智能家居集成商与现场调试人员的 Windows 组地址规划与交付工具。从设备规划、现场记录和 ETS6 XML 出发，把命名、地址、网关适配与交付资料连在一起。

[下载正式版](https://github.com/appleyancheng-art/KNX-FlowGen/releases/latest) · [官方网站与在线体验](http://knxflowgen.top:9920/ff/) · [购买激活码](https://68n.cn/E3Snb) · [中文手册](docs/KNX_FlowGen_User_Manual_CN.pdf) · [English manual](docs/KNX_FlowGen_User_Manual_EN.pdf)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/posters/dark-zh-preview.jpg">
  <source media="(prefers-color-scheme: light)" srcset="assets/posters/light-zh-preview.jpg">
  <img src="assets/posters/light-zh-preview.jpg" alt="KNX FlowGen 2.0：现场记录、五大适配器与工程交付" width="100%">
</picture>

这里展示的是**官网已上线的 2.0 正式版（2026-09-22 修订）**。GitHub 安装包与官网下载文件的 SHA-256 完全一致。软件面向 **Windows 10 / 11**；海报中的电脑与工程场景为合成展示，平台支持以软件说明为准。

## 三种起点，一条交付路径

| 项目情况 | 从哪里开始 | 接下来可以做什么 |
| --- | --- | --- |
| 新项目，尚未规划地址 | 设备规划 / 批量规划 | 选择功能、统一命名、生成地址、检查并导出 |
| 精装房、存量改造，已有实测地址 | 现场记录 Excel | 保留原地址，按设备与房间编辑，转译并交付 |
| 已有 ETS6 组地址表 | 导入 ETS6 XML | 辅助识别分类，复核 DPT 与功能，继续适配 |

一份项目数据，可以导出 **ETS6 组地址 XML**，进入 **五个网关与平台适配器**，也可以整理为 **PDF / Excel 交付清单**。

## 看见完整工作流程

以下为官网的完整中文界面图库。点击图片可查看原图；英文界面见后面的 English gallery。

### 01 · 设备规划：从功能点开始

按设备类型、数量与起始地址生成组地址。选择连续递增或层级结构，调整功能顺序、批量命名，也可以手动修改功能点名称并同步到相关输出。已有批次占用地址时，显示冲突与下一可用起始地址建议。

![设备规划：从功能点开始](assets/screenshots/product_shot_1.png)

### 02 · 批量规划：把整个项目放在一起

把不同房间、设备和功能组织为多个批次，集中检查、保存与导出 ETS6 XML。进入网关适配时，通过统一选择入口切换目标平台，不必为每个网关重新整理一份数据。

![批量规划：把整个项目放在一起](assets/screenshots/product_shot_2.png)

### 03 · 导入转换：让现场记录成为可交付项目

精装房与存量改造常常需要先在现场抓取地址。下载标准 Excel 模板，用下拉列表选择设备分类，记录设备、房间、功能、组地址与 DPT；导入后保留实测地址，继续编辑和检查。可以再次保存 Excel 补录，也可以输出 XML 或进入适配中心。

另一个入口支持 ETS6 导出的组地址 XML，结合名称与 DPT 辅助识别设备与功能。现场抓取由外部工具完成；未知 DPT、功能和读写映射需要人工确认。

![导入转换：让现场记录成为可交付项目](assets/screenshots/product_shot_3.png)

### 04 · 模板管理：把常用做法留下来

保存常用功能点顺序和设备配置，在后续规划中调用。结合项目保存、恢复与全局命名，让不同房间和批次沿用一致的工程习惯。

![模板管理：把常用做法留下来](assets/screenshots/product_shot_4.png)

### 05 · Thinka：导出前，把映射看清楚

选择数据来源和要导出的设备，核对房间、服务名称、服务类型及读写地址。无房间名称时提供可编辑的默认房间；更新已有配件时保留原 Accessory ID。正式版已修复 CSV 在 Excel 中打开的中文乱码。

![Thinka：导出前，把映射看清楚](assets/screenshots/product_shot_5.png)

### 06 · Home Assistant：集中生成 KNX YAML

在适配中心生成 Home Assistant KNX 配置。按数据来源筛选设备、核对实体字段和映射，统一导出 YAML。使用前结合实际 KNX 连接与 Home Assistant 配置复核。

![Home Assistant：集中生成 KNX YAML](assets/screenshots/product_shot_6.png)

### 07 · 项目检查：问题在交付前看见

检查地址重复、范围与缺失信息，结合预览核对 DPT 和命名。ETS6 XML 按层级分行显示，便于阅读与排查；辅助检查不能代替现场设备和总线验证。

![项目检查：问题在交付前看见](assets/screenshots/product_shot_7.png)

### 08 · 交付清单：一份资料，说明整个项目

自由组合设备规划、多个批次与导入地址，生成带 KNX FlowGen 品牌的 Excel 或 PDF 清单。保留来源、设备、房间、功能与地址信息，并标明待复核条目，方便归档、移交与后续维护。

![交付清单：一份资料，说明整个项目](assets/screenshots/product_shot_8.png)

## 五个网关与平台，一个适配中心

| 平台 / 网关 | 导出格式 | 使用重点 |
| --- | --- | --- |
| Thinka | Gateway CSV | 服务、特征、读写地址；新配件 ID 留空，更新时保留原 ID |
| Home Assistant | KNX YAML | 核对实体类型、DPT 与配置字段 |
| Pandora Edge Matter | XLS | 按原模板工作表映射并选择设备 |
| HDL KNX | XLS | 灯光、遮阳、空调、地暖与新风模板 |
| KGP Matter | 中英双语 XLSX | 保留原表头和设备续行结构 |

来源与设备可在适配中心选择，房间和必要参数可在导出前复核。各网关支持范围以目标模板和映射规则为准，未映射功能会提示。详见[适配说明](docs/ADAPTERS.md)。

## English interface gallery

KNX FlowGen is a Windows tool for KNX group-address planning, field-record imports, ETS6 XML conversion, gateway adaptation and project handover. The screenshots below show the English interface of the published 2.0 release.

<details>
<summary>View all 8 English screenshots / 展开完整英文界面</summary>

### 01 · Device planning and address suggestions

![Device planning and address suggestions](assets/screenshots/product_shot_en_1.png)

### 02 · Batch planning across rooms and devices

![Batch planning across rooms and devices](assets/screenshots/product_shot_en_2.png)

### 03 · Field records and ETS6 XML import

![Field records and ETS6 XML import](assets/screenshots/product_shot_en_3.png)

### 04 · Reusable templates

![Reusable templates](assets/screenshots/product_shot_en_4.png)

### 05 · Thinka Adapter Center

![Thinka Adapter Center](assets/screenshots/product_shot_en_5.png)

### 06 · Home Assistant Adapter Center

![Home Assistant Adapter Center](assets/screenshots/product_shot_en_6.png)

### 07 · Project review and XML preview

![Project review and XML preview](assets/screenshots/product_shot_en_7.png)

### 08 · PDF and Excel project handover

![PDF and Excel project handover](assets/screenshots/product_shot_en_8.png)

</details>

## 2.0 发布海报

来自既有宣传素材的“现场记录”修订版，保留原始比例与完整内容。中文、英文各有浅色和深色版本，点击下方链接可打开 3840 × 2160 原图。

| 中文 · 浅色 | 中文 · 深色 |
| --- | --- |
| ![中文浅色海报](assets/posters/light-zh-preview.jpg) | ![中文深色海报](assets/posters/dark-zh-preview.jpg) |
| [查看 4K 原图](assets/posters/light-zh-4k.png) | [查看 4K 原图](assets/posters/dark-zh-4k.png) |

| English · Light | English · Dark |
| --- | --- |
| ![English light poster](assets/posters/light-en-preview.jpg) | ![English dark poster](assets/posters/dark-en-preview.jpg) |
| [Open 4K original](assets/posters/light-en-4k.png) | [Open 4K original](assets/posters/dark-en-4k.png) |

海报包含场景合成与屏幕透视处理；上方产品图库提供实际界面截图。软件支持 Windows，海报中的笔记本外观不代表 macOS 原生版本。

## 下载与开始使用

1. 打开[正式版下载](https://github.com/appleyancheng-art/KNX-FlowGen/releases/latest)，下载 `KNX_FlowGen_Setup_v2.0.0.exe`。
2. 保存项目并退出旧版后安装。Windows 10 / 11 为主要使用目标，需安装 Edge 或 Chrome 109+。
3. 按软件提示激活，授权规则以[购买页面](https://68n.cn/E3Snb)为准。
4. 选择设备规划、现场记录或 ETS6 XML 导入，完成复核后导出。

当前安装包未代码签名，Windows 可能显示安全提示。Releases 自动生成的 `Source code (zip)` 是本展示仓库的资料归档，不能代替 EXE 安装包。

正式更新会同步官网、GitHub 下载与文档，安装包校验信息见 Releases。

## 手册与更新

- [中文用户手册 PDF](docs/KNX_FlowGen_User_Manual_CN.pdf)
- [English User Manual PDF](docs/KNX_FlowGen_User_Manual_EN.pdf)
- [适配器说明](docs/ADAPTERS.md)
- [2.0 更新记录](CHANGELOG.md)
- [常见问题](docs/FAQ.md)

## 联系与购买

作者：**做智能的姚老师**  
[购买激活码](https://68n.cn/E3Snb) · [抖音主页](https://v.douyin.com/2S7WNUvxeYs/) · [官网联系方式](http://knxflowgen.top:9920/ff/#contact)

问题反馈可在 [Issues](https://github.com/appleyancheng-art/KNX-FlowGen/issues) 提交。请附版本、操作步骤和脱敏截图，勿公开激活码、客户工程文件或个人信息。

## 使用与品牌

本仓库用于软件介绍、文档与安装包分发。**KNX FlowGen 是需要授权的软件，本仓库公开不代表程序源码开源。** 第三方品牌与标识属于各自权利人；列出适配不代表官方认证或合作关系。
