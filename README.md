<div align="center">
  <h1>MPScan</h1>

  <img width="128" height="128" alt="Yee Music" src="https://avatars.githubusercontent.com/u/109730978">
</div>

<div align="center">
  <p>MPScan 实现了从 自动提取 → 反编译 → 敏感信息识别 → 风险可视化 → 报告输出 的完整工作流</p>
  <p><strong>微信小程序安全审计一体化解决方案</strong></p>
</div>

<div align="center">
  <a href="https://github.com/i-am-xjizhi/MPScan/stargazers">
    <img src="https://img.shields.io/github/stars/i-am-xjizhi/MPScan" alt="GitHub Stars">
  </a>
  <a href="https://github.com/i-am-xjizhi/MPScan/network">
    <img src="https://img.shields.io/github/forks/i-am-xjizhi/MPScan" alt="GitHub Forks">
  </a>
  <a href="https://github.com/i-am-xjizhi/MPScan/watchers">
    <img src="https://img.shields.io/github/watchers/i-am-xjizhi/MPScan" alt="GitHub Watchers">
  </a>
  </b>
</div>

<div align="center">

[![Version][version-shield]][version-url]
[![OS][os-shield]][os-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]
[![Downloads Total][downloads-total-shield]][downloads-url]
[![Downloads Latest][downloads-latest-shield]][downloads-url]

[version-shield]: https://img.shields.io/badge/Version-3.0-blue?labelColor=black
[version-url]: #
[os-shield]: https://img.shields.io/badge/OS-Windows_10/11-0078D6?labelColor=black&color=blue
[os-url]: #
[issues-shield]: https://img.shields.io/github/issues/i-am-xjizhi/MPScan?labelColor=black&color=green&label=Issues
[issues-url]: https://github.com/i-am-xjizhi/MPScan/issues
[license-shield]: https://img.shields.io/badge/License-MIT-green.svg?labelColor=black&label=License
[license-url]: https://github.com/i-am-xjizhi/MPScan/tree/main?tab=MIT-1-ov-file
[downloads-total-shield]: https://img.shields.io/github/downloads/i-am-xjizhi/MPScan/total?labelColor=black&color=red&label=Downloads
[downloads-latest-shield]: https://img.shields.io/github/downloads/i-am-xjizhi/MPScan/latest/total?labelColor=black&color=red&label=Downloads%40Latest
[downloads-url]: https://api.github.com/repos/i-am-xjizhi/MPScan/releases

</div>


## 🖼️ 界面展示
> MPScan 是一款为安全研究人员与开发者设计的 Windows GUI 一体化工具，专用于对微信小程序进行自动化安全审计。基于对 wxapkg 反编译工具的深度二次开发与功能拓展，本工具实现了从 自动提取 → 反编译 → 敏感信息识别 → 风险可视化 → 报告输出 的完整工作流。

![图片](https://github.com/user-attachments/assets/3e12732e-a001-4963-a75f-1e1821000f8e)


---

## ✨ 工具亮点
```
📂 无缝双版本监控 – 自动适配新版与经典版微信，智能监控双份小程序包目录，确保资产无遗漏。
🚀 一键自动化 – 无需复杂配置，启动即用，覆盖监控、解包、扫描、分析完整流程。
🔍 深度内容识别 – 可自定义添加正则匹配条目，内置22条敏感信息规则，包括各类云服务密钥、数据库连接串、API Token、内网地址等。
🎨 直观风险呈现 – 采用三级色彩标记，结果清晰可读。支持点击查看上下文代码，并新增小程序官方图标辅助资产识别。
📦 开箱即用 – 纯原生 Windows 应用，无需安装 Python、Node.js 等任何外部依赖。
💼 高效操作流 – 提供结果表右键菜单（复制、打开、定位）、代码预览、实时日志跟踪及一键报告导出，极大提升分析效率。
🤝 生态联动 – 集成敏感信息利用工具（API-Explorer），实现扫描到利用的快速衔接。
``` 

---

## 🛠️ 核心功能
```
1. 双版本监控与自动反编译
自动监听并兼容新版与旧版微信的小程序包路径（%APPDATA%\Tencent\xwechat\... 及 %USERPROFILE%\Documents\WeChat Files\...）。
一旦有新的 .wxapkg 文件产生，立即自动触发反编译与安全扫描，实现“发现即审计”。
2. 资产识别增强
自动解析并显示小程序名称（优化解析逻辑，减少乱码与wxid显示）。
新增结果显示微信小程序官方图标，即使在名称解析失败时也能辅助确认资产归属。
3. 批量扫描与手动分析
支持手动选择小程序包目录进行批量处理。
适用于专项安全审计、合规检查或对历史小程序的批量排查。
4. 强化敏感信息提取
优化扫描引擎，修复AK/SK漏报，提升大文件与长行文本处理能力。
内置专用于微信生态与常见云服务的正则规则库，精准识别超过20类高风险敏感信息。
5. 交互式代码审查面板
点击任意扫描结果条目，中央面板实时展示该敏感信息所在的源代码及位置。
默认显示命中代码行的前后各20行上下文，辅助人工研判风险与排除误报。
6. 实时扫描日志
日志面板优先显示最新条目，便于实时跟踪扫描进度与状态。
修复并优化分包解包等环节的提示信息，减少误报。
7. 便捷的右键操作菜单
在结果列表中右键点击任意条目，可快速执行以下操作：
  复制内容：复制选中的敏感信息文本。
  用记事本打开：直接打开包含该信息的源文件。
  在资源管理器中定位：快速跳转至源文件所在文件夹。双版本监控与自动反编译
8. 一键导出报告
支持将完整扫描结果导出为CSV格式报告。
文件编码兼容Microsoft Excel，确保中文内容无乱码，便于存档、分享或进一步数据处理。
9. 外围工具快捷启动
界面集成「利用工具」快捷入口，可一键启动同目录下的API-Explorer工具，实现从信息发现到利用验证的快速流转。
```

---

## 📁 覆盖的敏感信息类型

| 类别 | 识别示例 |
|------|----------|
| 微信生态 | AppSecret、支付密钥（mch_key）、商户号（mch_id） |
| 腾讯云 | SecretId、SecretKey、COS 存储桶配置、短信服务密钥 |
| 阿里云 | AccessKey ID、AccessKey Secret、OSS 配置 |
| AWS | AWS_ACCESS_KEY_ID、AWS_SECRET_ACCESS_KEY |
| 其他云服务 | 七牛云 AK/SK、华为云 AK/SK、百度云 AK/SK |
| 数据库 | MongoDB 连接 URL、MySQL 连接字符串、Redis 连接地址与密码 |
| 通用密钥令牌 | API Key、JWT Token、Password、Bearer Token、私钥文件路径 |
| 网络与内网信息 | 内网 IP 地址（10.x，172.16.x，192.168.x）、硬编码的未授权访问端点 |

---

## ⚙️ 运行环境与使用

```
操作系统：Windows 10 / 11 （64位）
环境要求：无需安装任何依赖（如Python、Node.js、Java等）。下载可执行文件，解压后双击即可运行。
```

---

## 🚀 快速开始
```
下载发布版本：从 Releases 页面下载最新的 MPScan.zip。
解压运行：解压到任意目录，双击运行 MPScan.exe。
开始扫描：
自动监控模式：启动后，工具将自动开始监控。当微信有新小程序运行时，会自动扫描。
手动扫描模式：点击“选择目录”，手动指定包含 .wxapkg 文件的文件夹进行批量扫描。
查看与导出结果：在界面中查看分级风险结果，点击条目查看代码上下文，可通过右键菜单或“导出”按钮生成报告。
```

![图片](https://github.com/user-attachments/assets/9ee0dafb-5203-49e1-ae0e-8803272fd0d6)

![图片](https://github.com/user-attachments/assets/dc058f19-e6c3-4285-9f60-048d9ed4fb81)

![图片](https://github.com/user-attachments/assets/64f7d532-b21a-49cf-98c9-5abe600696a2)

![图片](https://github.com/user-attachments/assets/3e12732e-a001-4963-a75f-1e1821000f8e)
  

---

## 🙏 致谢

感谢所有为本项目做出贡献的开发者！

---

## ⚠️ 免责声明

本工具仅供安全研究和授权测试使用。使用本工具进行未经授权的测试是违法的。使用者需自行承担使用本工具的一切后果，作者不承担任何法律责任。

---

## 📋 更新日志

| 版本 | 日期 | 说明 |
|------|------|------|
| **v3.0** | 20260729 | **主要更新** |
| | | **新增** |
| | | • **结果表显示小程序官方图标**：在小程序名称列前新增图标列，使用微信本地缓存图标展示。当名称解析失败时，用户仍可通过图标确认资产归属。实现上采用相对路径推导、智能匹配最新图标、纯库图像处理与高效缓存，界面绘制零IO。 |
| | | • **自动识别新版微信监控目录**：新增 `findXWeChatAppletPackage()` 函数，自动扫描 `%APPDATA%\Tencent\xwechat\radium\...` 路径，解决安装新版微信后工具打开为空的问题。 |
| | | **修复** |
| | | • **运行白屏问题**：修复特定环境下启动后界面白屏的兼容性问题。 |
| | | • **分包解包误报**：优化检测逻辑，减少因临时文件导致的误报提示。 |
| | | • **运行日志排序**：日志面板现优先显示最新条目，便于实时跟踪扫描进度。 |
| | | • **AK/SK部分漏报修复**：解决因文件大小、缓冲区和匹配逻辑导致的静默跳过问题。具体修复：1) 文件大小上限提升至64MB；2) `bufio.Scanner` 替换为 `bufio.Reader.ReadString`，避免超长行被截断；3) 匹配函数改为 `FindAllStringSubmatch`，确保提取所有匹配项。 |
| **v2.0** | 20260423 | **主要更新** |
| | | **新增** |
| | | • **敏感信息利用工具集成**：界面右下角新增「利用工具: API-Explorer_v2.1.0」快捷入口。鼠标悬停显示安全提示，双击可直接启动同目录下的 `API-Explorer_v2.1.0.exe`；若工具未就位则弹窗提示下载地址。 |
| | | **修复** |
| | | • **小程序名称识别错误**：修复部分小程序中文名称无法正确显示、显示为 wxid 或乱码的问题。优化名称解析逻辑，按优先级依次读取 `app-config.json` → `project.config.json` → `app.json`，与官方数据保持一致。 |
| **v1.0** | 初始版本 | **基础功能** |
| | | • 支持微信小程序 .wxapkg 自动监控与反编译。 |
| | | • 敏感信息扫描：覆盖云密钥、数据库连接串、API Token、内网 IP 等 20+ 规则。 |
| | | • 结果可视化展示，支持代码上下文预览与 CSV 导出。 |

---

## 💬 互动交流
欢迎加入我们的安全技术交流群，与开发者和安全研究人员一起讨论安全工具的使用、漏洞挖掘等话题！

### 🤝 加入技术交流群
- 微信群（推荐）

![微信群](https://github.com/user-attachments/assets/129399c3-272f-48f2-ad68-2080c7357b22)

- ➕V：xjizhi_run 进入GG安全交流群（**交流群超200人需要人工邀请，扫码+V时请备注：进群**）
- 微信二维码

![微信](https://github.com/user-attachments/assets/ab7fbf45-dfd4-40c9-b53e-00b3f92e3e90)

### 📧 联系方式
如有任何问题或建议，也可以通过以下方式联系：
- **GitHub Issues**: [提交 Issue](https://github.com/i-am-xjizhi/MPScan/issues)
