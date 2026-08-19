[English](../en/faq.md) · [简体中文](../zh-Hans/faq.md) · **繁體中文** · [Deutsch](../de/faq.md)

---

# 常見問題

## 關於

### OtterPix 是什麼？

一款 Mac 影像工具箱：十個一鍵基本工具（轉檔、壓縮、調整大小、裁切、旋轉、浮水印、重新命名、後設資料、PDF 轉圖片、QR Code），一條可批次處理的視覺化[處理流程](pipeline.md)，以及七項裝置端 AI 功能。一切都在 Apple 晶片上本機執行——不需帳號、不上傳任何內容。

### OtterPix 是開源的嗎？

不是。OtterPix 是一款透過 Mac App Store 發行的商業閉源 App——這個儲存庫不含原始碼，未來也沒有開源的計畫。這裡是這款 App 的公開基地：使用指南、發行說明與錯誤追蹤。

### OtterPix 支援哪些語言？

App 介面共提供 18 種語言。本儲存庫的指南以四種語言維護：English、简体中文、繁體中文、Deutsch。18 種語言中任何翻譯錯誤或不通順之處都值得[開一個 Issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose)——母語者的修正經常在下一個版本就上線。

### 系統需求是什麼？

macOS 14（Sonoma）或更新版本，Apple 晶片 Mac（M1 或更新）。不支援 Intel Mac。AI 圖片生成建議 16 GB 以上記憶體。

## 格式與檔案

### OtterPix 能讀寫哪些格式？

讀與寫：JPEG、PNG、TIFF、BMP、HEIC、WebP、AVIF——轉換選單中另有**其他格式**區，收錄你的 Mac 能寫出的較少見格式。可讀取的範圍更廣：首頁拖放區標示 PNG · JPEG · HEIC · TIFF · WebP · GIF +51。PDF 可用 [PDF 轉圖片](tools/pdf-and-qr.md)工具以任意 DPI 轉存為圖片。

### 色彩描述檔與 EXIF 方向會保留嗎？

大多數操作都會保留色彩描述檔與 EXIF 方向。唯一會移除後設資料的，正是為此而設計的功能：[後設資料](tools/metadata.md)工具的清除功能，以及流程中的**清除後設資料**步驟。

### OtterPix 會改動我的原始檔案嗎？

沒有任何工具會覆寫原始檔案。儲存永遠是把副本寫到你選擇的位置；批次重新命名同樣寫入你指定的資料夾，除非你主動開啟**將原檔案移到垃圾桶**，否則原始檔案留在原位。

## 隱私與網路

### OtterPix 會上傳我的圖片嗎？

不會。每一項操作——包括 AI 推論——都在你的 Mac 上本機執行。App 不含分析 SDK，也絕不會上傳圖片、生成提示詞、OCR 內容或使用情況遙測資料。有限的連線用途包括 StoreKit；啟動時僅用於選擇模型下載鏡像的 Cloudflare 邊緣國家代碼查詢；首次使用模型商店時更新只包含下載 URL 的小型清單；以及你主動發起的模型下載。這些請求都不含你的媒體或處理內容。完整說明見[隱私政策](https://otterpix.app/zh-Hant/privacy)。

### 可以離線使用 OtterPix 嗎？

可以。基本處理和已下載模型的 AI 推論都可離線運作。首次或更新模型，以及購買或回復購買時仍需連線；上述後設資料和路由請求不會上傳處理內容。

### 分享照片前要怎麼移除 GPS 資料？

用[後設資料](tools/metadata.md)工具：**移除 GPS** 開關只去掉位置資訊；或用**隱私**清除預設，一次清除 GPS 加上相機型號、鏡頭、創作者，同時保留日期、曝光與方向。

## AI 模型

### 為什麼 AI 功能要下載東西？

每項 AI 功能都由一個模型驅動，模型與 App 分開發布，好讓 App 本體保持輕巧。第一次執行某項功能時，它會抓取自己的模型；之後該功能完全離線運作。體積從幾 MB（最小的超分模型）到數 GB（圖片生成）不等。

### 在哪裡管理模型？

**設定 → AI**。每個模型都能在那裡下載或刪除；進行中的下載可以暫停、繼續或取消。部分資料會跨重新啟動保留，並顯示為可繼續，而不會冒充已安裝；功能頁面會同步顯示所需模型的同一進度。

### 模型要收費嗎？

不用。所有功能的模型下載都是免費的，包括 Pro 工具。

## 免費與 Pro

### 到底哪些是免費的？

全部十個基本工具、處理流程、AI 文字辨識與 AI 圖片生成——永久免費，不是試用。此外，五個 Pro AI 工具（AI 超分、AI 去背、AI 消除、AI 隱私模糊、AI 人像修復）每天各含 1 次免費使用。

### 每日免費次數怎麼運作？

當免費次數還在時，每張 Pro AI 卡片會掛著琥珀色的**今日免費**徽章。成功執行一次後，橫幅會顯示：「本功能今日免費次數已用完」——「每個 AI 功能每天各有 1 次免費，本功能將在午夜恢復。」次數按載入的照片計算，不是按點選次數：同一張照片整天都能重跑、調整、反覆修，都算那一次；當天已用過免費次數的照片，切換回來仍可免費繼續調整。

### 流程的免費版限制是什麼？

「免費版:含 Pro 步驟的管線僅限 1 張圖。升級可批次處理。」——每條流程限一個 Pro 步驟、鏈上有 Pro 步驟時僅限單張圖片，執行它會消耗該工具的每日免費次數。詳見[處理流程指南](pipeline.md#免費版限制)。

### Pro 多少錢？怎麼管理？

Pro 提供月訂閱、年訂閱，或一次性買斷——目前定價請見 [Mac App Store](https://apps.apple.com/app/id6772468615)。訂閱在你的 [Apple 帳號訂閱頁面](https://apps.apple.com/account/subscriptions)管理或取消。買斷為一次性付費：不會續訂，也沒有需要管理的訂閱。

### 退款怎麼處理？

所有購買都由 Apple 處理，退款申請請透過 Apple 的 [reportaproblem.apple.com](https://reportaproblem.apple.com) 提出。開發者看不到你的付款資料，也無法直接退款。

## 地區供應與支援

### 每個國家都有全部功能嗎？

透過中國大陸區 Mac App Store 發行的 OtterPix 版本不提供 AI 圖片生成與 AI 文字辨識。其餘全部功能（包括五項 Pro AI 功能）在 OtterPix 上架的所有地區均可使用。詳見[服務條款](https://otterpix.app/zh-Hant/terms)。

### 在哪裡回報錯誤、提出問題？

錯誤 → [開一個 Issue](https://github.com/nanguoyu/OtterPix-app/issues/new/choose)。問題 → [Discussions → Q&A](https://github.com/nanguoyu/OtterPix-app/discussions/categories/q-a)。English、中文、Deutsch 都歡迎。私人或敏感事項：hello@otterpix.app。

## 另請參閱

- [快速上手](getting-started.md)
- [處理流程](pipeline.md)
- [更新日誌](changelog.md)

---

**意見回饋**——錯誤請到 [Issues](https://github.com/nanguoyu/OtterPix-app/issues/new/choose) 回報；問題請到 [Discussions](https://github.com/nanguoyu/OtterPix-app/discussions) 發問。
