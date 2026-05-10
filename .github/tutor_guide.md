針對 **`01-unit-vscode-online` (VS Code Online 快速啟動)** 單元，這個單元的 Assignments (作業) 目標是讓學生理解「瀏覽器即開發環境」的操作流程。

以下是在 **GitHub Classroom** 部署這三個實戰任務的具體建議：

### 1. 核心設置：啟用 GitHub Codespaces 支援
在建立 Classroom 作業時，請務必在設定頁面中勾選 **"Enable GitHub Codespaces"**。這能讓學員獲得免費的雲端運算時數，且無需在本地安裝任何軟體即可完成作業。

---

### 2. 作業任務部署細節

#### 任務 1：Web Serial 硬體連線測試 (Web Serial Lab)
*   **目標**：練習使用 `vscode.dev` (快捷鍵 `.`) 讀取 ESP32 訊號。
*   **Classroom 部署建議**：
    *   **Template 程式庫**：提供一個 `serial-log.md` 檔案。
    *   **驗證方式**：要求學生將從 Web Serial 監控視窗看到的 "Hello" 原始數據截圖或複製內容，貼入 `serial-log.md` 並執行 `push`。這能確認他們真的有成功建立「瀏覽器 - 硬體」的通訊路徑。

#### 任務 2：Codespaces 雲端編譯實戰 (Cloud Build Lab)
*   **目標**：在雲端 Container 中執行 Linux 指令。
*   **Classroom 部署建議**：
    *   **Template 程式庫 (關鍵！)**：包含 `.devcontainer/` 資料夾。在其中的 `devcontainer.json` 設置 `postCreateCommand`: `"npm install"`，模擬專業工作流。
    *   **自動評分 (Autograding)**：
        *   提供一個 `cloud-test.js`。
        *   要求學生執行 `node cloud-test.js > test-result.log`。
        *   **Autograding 腳本**：檢查 `test-result.log` 是否包含預期文字（如「雲端環境運行成功」）。

#### 任務 3：跨裝置同步除錯挑戰 (Cross-Device Sync)
*   **目標**：體驗雲端開發的「接力」特性。
*   **Classroom 部署建議**：
    *   **操作規則**：引導學生在手機端按下 `.` 進入編輯，並在 Commit Message 中明確註明 `[Mobile Edit]` 字樣。
    *   **導師評量 (Tutor Review)**：導師只需在 Classroom Dashboard 查看 Commit History，看到有來自不同裝置特徵的提交紀錄，即可打分。這也順便訓練了學生撰寫「有意義 Commit Message」的習慣。

---

### 3. 導師管理精選工具
*   **範本目錄建議 (Template Structure)**：
    ```text
    .
    ├── .devcontainer/    # 確保 Codespace 環境預裝好 Node.js
    ├── src/
    │   └── main.js
    ├── cloud-test.js     # 任務 2 測試腳本
    ├── serial-log.md     # 任務 1 回報檔案
    └── instructions.md   # 任務 3 的跨裝置操作指南
    ```
*   **回饋建議**：本單元非常適合使用 **"Inline Comments"**。導師可以在學生提交的代碼中標註：「看到你在手機端也完成提交了，這就是雲端開發的靈活性！」。

這套部署方案能讓學生直接感受到「雲端開發 (Codespaces)」與「本地開發 (Desktop)」在工作流上的巨大差異，同時降低了學員因電腦配備不足而產生的學習門檻。
