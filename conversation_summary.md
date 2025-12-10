# 對話摘要 (Conversation Summary)

本次對話的目的是建立一個簡單的 **AI / Human 文章偵測器 (AI Text Detector)**。

## 任務目標

-   開發一個能夠接收使用者輸入文本的工具。
-   判斷該文本是 AI 生成還是人類撰寫，並顯示 AI 與 Human 的百分比。
-   使用 `Streamlit` 作為使用者介面 (UI)。
-   利用 `sklearn`、`transformers` 或自建特徵法作為文本分類的核心技術。

## 執行過程

1.  **選擇技術棧**：決定使用 `Streamlit` 快速建立 UI，並採用 `transformers` 函式庫中的預訓練模型 `roberta-base-openai-detector` 作為核心分類器，以提供高效且準確的偵測能力。
2.  **建立 `requirements.txt`**：創建了包含 `streamlit`、`transformers`、`torch` 和 `sentencepiece` 等必要依賴的檔案，以確保應用程式可以順利運行。
3.  **開發 `app.py`**：編寫了 Streamlit 應用程式的核心邏輯，包括：
    -   載入 `roberta-base-openai-detector` 模型（使用 `@st.cache_resource` 進行快取）。
    -   設計友善的使用者介面，包含標題、說明、文本輸入框和「分析文本」按鈕。
    -   處理用戶輸入，調用模型進行預測。
    -   將模型輸出轉換為易於理解的 AI% / Human% 格式，並在 UI 上視覺化呈現結果。
4.  **提供執行指南**：詳細說明了如何安裝相依套件 (`pip install -r requirements.txt`) 以及如何啟動 Streamlit 應用程式 (`streamlit run app.py` 或 `python -m streamlit run app.py`)。同時提醒了首次運行時模型下載可能需要時間。
5.  **編寫專案概要**：根據使用者要求，撰寫了 `README.md` 檔案，提供了專案的完整概覽、技術細節和操作說明。

## 成果

成功建立了 `requirements.txt`、`app.py` 和 `README.md` 等檔案，並提供了啟動和使用該 AI 文章偵測器的完整說明。使用者現在可以按照 `README.md` 中的指示運行此應用程式。
