[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-live-2ea44f?logo=github)](https://dimillian.github.io/Skills/)

# Skills Public

專為 iOS 和 Swift 開發工作流程設計的專業技能集合。

## 概述

此儲存庫包含一組專注的技能，旨在協助常見的 iOS 開發任務，從生成版本說明到除錯應用程式和維護程式碼品質。

## 安裝

### 透過 GitHub（建議）
1. 在 Claude Code 中執行 `/plugin`
2. 選擇「Add Marketplace」
3. 輸入 `dimillian/Skills`（或您的 fork）
4. 然後安裝：`/plugin install ios-mac-skills@ios-mac-skills`

### 手動安裝
1. 複製此儲存庫
2. 在 Claude Code 中執行 `/plugin`
3. 選擇「Install from local folder」
4. 選擇已複製的資料夾

### 開發設定
可選：啟用 pre-commit hook 以保持 `docs/skills.json` 同步：
`git config core.hooksPath scripts/git-hooks`

## 技能

### 📝 App Store 更新日誌

**用途**：從 git 歷史記錄生成面向使用者的 App Store 版本說明。

自動收集自上次 git 標籤（或指定的參考點）以來的提交和變更，並將其轉換為清晰、以效益為導向的版本說明，適用於 App Store。過濾掉僅供內部使用的變更，並按主題分組使用者可見的改進。

**主要功能**：
- 收集自上次標籤以來的提交和修改的檔案
- 識別使用者可見的變更與內部工作
- 生成簡潔、以效益為導向的要點
- 驗證變更對應到實際提交

**使用時機**：當您需要根據 git 歷史記錄建立 App Store「新功能」文字或版本說明時。

---

### 🐛 iOS 除錯代理

**用途**：使用 XcodeBuildMCP 在模擬器上建置、執行和除錯 iOS 專案。

提供完整的工作流程，用於建置 iOS 應用程式、在模擬器上啟動、與 UI 互動以及擷取日誌。處理模擬器發現、工作階段設定和執行時除錯。

**主要功能**：
- 發現和管理已啟動的模擬器
- 在模擬器上建置和執行應用程式
- 與 UI 互動（點擊、輸入、滑動、手勢）
- 擷取和分析應用程式日誌
- 螢幕截圖和 UI 檢查

**使用時機**：當您需要執行 iOS 應用程式、與模擬器 UI 互動、檢查螢幕狀態或診斷執行時行為時。

---

### 🧭 GH Issue 修復流程

**用途**：使用 `gh`、本地編輯、建置/測試和 git push 端對端解決 GitHub issue。

提供結構化流程，用於讀取 issue、實作修復、使用 XcodeBuildMCP 驗證，以及提交關閉訊息並推送變更。

**主要功能**：
- 使用 `gh issue view` 取得完整的 issue 上下文
- 引導程式碼發現和專注編輯
- 透過 XcodeBuildMCP 執行針對性建置/測試
- 提交關閉訊息並推送

**使用時機**：當您需要取得 issue 編號、使用 `gh` 檢查、實作修復、執行測試並推送時。

---

### ⚡ Swift 並行專家

**用途**：檢查和修復 Swift 6.2+ 程式碼庫的 Swift 並行問題。

應用 actor 隔離、Sendable 安全性和現代並行模式來解決編譯器錯誤並提高並行合規性。專注於最小化行為變更，同時確保資料競爭安全。

**主要功能**：
- 識別 actor 上下文和隔離問題
- 應用安全修復，保留現有行為
- 處理 UI 綁定類型、協議和背景工作
- 確保 Sendable 合規性

**使用時機**：當您需要檢查 Swift 並行使用、提高並行合規性或修復 Swift 並行編譯器錯誤時。

---

### 💎 SwiftUI Liquid Glass

**用途**：使用 iOS 26+ Liquid Glass API 實作和檢查 SwiftUI 功能。

協助在 SwiftUI 介面中採用原生 Liquid Glass API，確保正確使用、效能和設計一致性。支援新實作和重構現有功能。

**主要功能**：
- 使用原生 `glassEffect` 和 `GlassEffectContainer` API
- 確保正確的修飾符順序和組合
- 處理 iOS 26+ 可用性及向下相容
- 為可點擊元素實作互動式玻璃效果
- 支援變形轉場

**使用時機**：當您需要在新的 SwiftUI UI 中採用 Liquid Glass、將現有功能重構為 Liquid Glass，或檢查 Liquid Glass 使用是否正確時。

---

### 🧩 SwiftUI UI 模式

**用途**：建構 SwiftUI 視圖和元件的最佳實踐和範例驅動指南。

提供結構化的視圖組合、狀態所有權和元件選擇方法，包含常見模式的參考和腳手架指南。

**主要功能**：
- TabView、NavigationStack、Sheets 等元件參考
- 新應用程式佈線的腳手架指南
- 強調 SwiftUI 原生狀態和組合
- 一致、可維護的視圖結構指南

**使用時機**：當您需要幫助設計 SwiftUI UI、組合畫面或選擇元件模式時。

---

### 🔧 SwiftUI 視圖重構

**用途**：重構 SwiftUI 視圖檔案以獲得一致的結構和相依性模式。

將標準化排序、Model-View（MV）模式和正確的 Observation 使用應用於 SwiftUI 視圖。專注於使視圖輕量、可組合和可維護。

**主要功能**：
- 強制一致的視圖排序（Environment → State → init → body → helpers）
- 盡可能推廣 MV 模式而非 view models
- 安全處理 view models（盡可能非可選）
- 確保正確的 `@Observable` 和 `@State` 使用
- 透過 `@Environment` 支援相依性注入

**使用時機**：當您需要清理 SwiftUI 視圖的結構、安全處理 view models，或標準化相依性注入和 Observation 使用時。

---

### 🚀 SwiftUI 效能稽核

**用途**：從程式碼審查和架構稽核並改善 SwiftUI 執行時效能。

專注於識別視圖程式碼和資料流中常見的 SwiftUI 效能陷阱，建議針對性重構，並在程式碼審查不足時引導使用者執行 Instruments 分析。

**主要功能**：
- 優先進行程式碼審查以解決緩慢渲染、卡頓捲動和過度更新
- 針對常見的 SwiftUI 陷阱（不穩定的 identity、繁重的 `body`、佈局抖動）
- 提供修復指南和重構建議
- 在需要時提供使用者執行的 Instruments 工作流程

**使用時機**：當您需要診斷 SwiftUI 效能問題、提高視圖/更新效率，或獲得 Instruments 分析指南時。

---

### 🧰 macOS SwiftPM 應用程式打包（無需 Xcode）

**用途**：無需 Xcode 專案即可建立、建置和打包基於 SwiftPM 的 macOS 應用程式。

引導建立最小的 SwiftPM macOS 應用程式資料夾，然後使用 shell 腳本建置、組裝 .app 套件、簽署，以及可選的公證或生成 Sparkle appcast。

**主要功能**：
- SwiftPM macOS 應用程式佈局的引導模板
- 無需 Xcode 即可組裝 .app 套件的打包腳本
- 打包和啟動應用程式的開發循環腳本
- 可選的發布簽署/公證和 appcast 工具

**使用時機**：當您需要從頭開始建立 macOS 應用程式佈局和打包流程而無需 Xcode 時。

---

## 使用方式

每個技能都是獨立的，擁有自己的文件。請參閱每個技能目錄中的 `SKILL.md` 檔案以獲取詳細的工作流程、指南和範例。

## 貢獻

技能設計為專注且可重複使用。添加新技能時，請確保它們：
- 具有清晰、單一的目的
- 包含完整的文件
- 遵循與現有技能一致的模式
- 在適用時包含參考資料
