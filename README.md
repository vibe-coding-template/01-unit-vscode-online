# VS Code Online 快速啟動

歡迎來到本單元的作業！本作業的目標是讓你理解「瀏覽器即開發環境」的操作流程，並學會如何在雲端與不同裝置間無縫切換開發環境。

## 實戰任務

請依序完成以下三個任務，並確保將你的修改提交（Push）回此程式庫。

---

### 任務 1：Codespaces 一鍵啟動與測試驗證 (Codespaces Boot Lab)
*   **目標**：在不依賴本機環境的情況下，完成雲端開發環境啟動與第一次測試循環。
*   **操作步驟**：
    1. 在本程式庫頁面點擊「Code」綠色按鈕，切換到「Codespaces」標籤頁，並點擊「Create codespace on main」。
    2. 等待雲端環境啟動完成（首次建立可能需要 1-3 分鐘）。
    3. 在終端機執行：
       ```bash
       npm install
       node cloud-test.js > test-result.log
       ```
    4. 參考 `codespaces-lab-report.md`，填入你的啟動時間、遇到問題與修正紀錄。
    5. 將 `test-result.log` 與 `codespaces-lab-report.md` 一起 `Commit` 並 `Push`。

### 任務 2：Codespaces 雲端編譯實戰 (Cloud Build Lab)
*   **目標**：在雲端 Container 中執行 Linux 指令。
*   **操作步驟**：
    1. 在本程式庫頁面點擊「Code」綠色按鈕，切換到「Codespaces」標籤頁，並點擊「Create codespace on main」。
    2. 等待雲端環境啟動（預計會自動執行 `npm install`）。
    3. 在下方終端機 (Terminal) 執行以下指令：
       ```bash
       node cloud-test.js > test-result.log
       ```
    4. 將產生的 `test-result.log` 檔案進行 `Commit` 與 `Push`。

### 任務 3：跨裝置同步除錯挑戰 (Cross-Device Sync)
*   **目標**：體驗雲端開發的「接力」特性。
*   **操作步驟**：
    1. 詳細操作指南請參閱 [instructions.md](instructions.md)。
    2. **核心挑戰**：先在電腦端對 `src/main.js` 修改（不要 Commit），接著拿起手機登入 GitHub 進入編輯模式，你會看到剛才修改的內容。
    3. 在手機端完成修改並提交，請務必在 Commit Message 中註明 `[Mobile Edit]` 字樣。

---

## 提交說明
* 確保所有任務要求的檔案（`codespaces-lab-report.md`、`test-result.log`）都已成功提交到此程式庫。
* 導師將根據你的 Commit 紀錄、Commit Message 以及檔案內容進行評分。
* 本單元旨在讓你感受「雲端開發 (Codespaces)」與「本地開發 (Desktop)」在工作流上的差異。

祝你順利完成任務！
