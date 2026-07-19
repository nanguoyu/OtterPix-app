[English](../en/faq.md) · **简体中文** · [繁體中文](../zh-Hant/faq.md) · [Deutsch](../de/faq.md)

---

# 常见问题

## 关于

### OtterPix 是什么？

一款 Mac 图像工具箱：十个一键式基础工具（转格式、压缩、缩放、裁剪、旋转、水印、重命名、元数据、PDF 转图片、二维码），一条可视化的批量[流水线](pipeline.md)，以及七项本地 AI 功能。一切都在 Apple 芯片上本地运行——无需账号，不上传任何内容。

### OtterPix 开源吗？

不开源。OtterPix 是一款通过 Mac App Store 分发的商业闭源应用——本仓库不包含源代码，也没有开源计划。这里是它面向用户的公开主页：使用指南、更新说明和问题追踪。

### OtterPix 支持哪些语言？

应用界面支持 18 种语言。本仓库的指南维护四种：English、简体中文、繁體中文、Deutsch。18 种语言里任何生硬或错误的翻译都值得[提一个 Issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose)——母语者的修正通常会在下一个版本发布。

### 系统要求是什么？

macOS 14（Sonoma）或更高版本，Apple 芯片 Mac（M1 或更新）。不支持 Intel Mac。使用 AI 图片生成建议 16 GB 及以上内存。

## 格式与文件

### OtterPix 能读写哪些格式？

读写：JPEG、PNG、TIFF、BMP、HEIC、WebP、AVIF——格式选择器里还有**其他格式**区，列出你的 Mac 能写出的更多小众格式。可读取的范围更广：主页拖放区标着 PNG · JPEG · HEIC · TIFF · WebP · GIF +51。PDF 可以用 [PDF 转图片](tools/pdf-and-qr.md)工具以任意 DPI 渲染为图片。

### 色彩配置文件和 EXIF 方向会保留吗？

绝大多数操作都会保留色彩配置文件和 EXIF 方向。唯一会去除元数据的，正是专门为此设计的功能：[元数据](tools/metadata.md)工具的清除功能，以及流水线的**清除元数据**步骤。

### OtterPix 会改动我的原始文件吗？

没有任何工具会覆盖原文件。保存永远是把副本写到你选择的位置；批量重命名同样写入你指定的文件夹，除非你主动勾选**将原文件移到废纸篓**，否则原文件原地保留。

## 隐私与联网

### OtterPix 会上传我的图片吗？

不会。每一项操作——包括全部 AI 功能——都在你的 Mac 上本地运行。应用不含统计分析 SDK，没有遥测，不上传图片。它运行在沙盒中，网络权限只覆盖两件事：首次使用 AI 功能时下载模型文件，以及 App Store 购买验证。完整说明见[隐私政策](https://otterpix.app/zh/privacy)。

### 可以离线使用 OtterPix 吗？

可以。基础工具从第一次启动起就离线可用。每项 AI 功能只需要联网一次——首次下载它的模型——之后永远离线运行。

### 分享照片前怎么去掉 GPS 位置信息？

用[元数据](tools/metadata.md)工具：**移除 GPS** 开关只去掉位置信息；**隐私**清除预设则去除 GPS 及相机型号、镜头、创作者，同时保留日期、曝光和方向。

## AI 模型

### 为什么 AI 功能要下载东西？

每项 AI 功能背后都有一个模型，模型与应用分开分发，以保持安装包小巧。首次运行某项功能时会下载它的模型；此后该功能完全离线工作。模型大小从几 MB（最小的超分模型）到数 GB（图片生成）不等。

### 在哪里管理这些模型？

**设置 → AI**。每个模型都能在那里下载、重新下载或删除——删除可释放磁盘空间，下次要用时应用会再次请求下载。

### 模型收费吗？

不收费。所有功能的模型下载都免费，包括 Pro 工具的模型。

## 免费与 Pro

### 到底哪些是免费的？

全部十个基础工具、流水线、AI 文字识别和 AI 图片生成——永久免费，不是试用。此外，五个 Pro AI 工具（AI 超分、AI 抠图、AI 擦除、AI 隐私模糊、AI 人像修复）每个每天各含 1 次免费使用。

### 每天的免费次数怎么计算？

某个 Pro AI 工具的免费次数还没用时，它的卡片显示琥珀色**今日免费**角标。成功运行一次后，横幅会提示：“本功能今日免费次数已用完”——“每个 AI 功能每天各有 1 次免费，本功能将在午夜恢复。”次数按“载入的照片”计，不按点击计：同一张照片当天可以反复运行、反复调整，都算这一次；当天已经用过免费次数的那张照片，切走再切回来仍然可以继续免费编辑。

### 流水线里免费版有什么限制？

“免费版:含 Pro 步骤的管线仅限 1 张图。升级可批量处理。”——每条流水线限 1 个 Pro 步骤，链上有 Pro 步骤时一次只能处理 1 张图，运行它消耗该工具当天的免费次数。详见[流水线指南](pipeline.md#免费版限制)。

### Pro 怎么收费，怎么管理？

Pro 提供包月订阅、包年订阅和一次性买断三种方式——当前价格见 [Mac App Store](https://apps.apple.com/app/id6772468615)。订阅在 [Apple 账户的订阅页面](https://apps.apple.com/account/subscriptions)管理和取消。买断为一次性付费：不会续费，也没有需要管理的订阅。

### 退款怎么办理？

所有购买均由 Apple 处理，退款请通过 Apple 的 [reportaproblem.apple.com](https://reportaproblem.apple.com) 申请。开发者看不到你的支付信息，也无法直接办理退款。

## 地区可用性与支持

### 每个国家/地区的功能都一样吗？

通过中国大陆区 Mac App Store 分发的 OtterPix 版本不提供 AI 图片生成与 AI 文字识别。其余全部功能（包括五项 Pro AI 功能）在 OtterPix 上架的所有地区均可使用。详见[服务条款](https://otterpix.app/zh/terms)。

### 在哪里报告 Bug 或提问？

Bug → [提交 Issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose)。提问 → [Discussions → Q&A](https://github.com/nanguoyu/OtterPix-app/discussions/categories/q-a)。中文、English、Deutsch 都欢迎。涉及隐私或敏感内容：hello@otterpix.app。

## 相关页面

- [快速上手](getting-started.md)
- [流水线](pipeline.md)
- [更新日志](changelog.md)

---

**反馈** — Bug 请到 [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) 报告；使用问题请到 [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions) 提问。
