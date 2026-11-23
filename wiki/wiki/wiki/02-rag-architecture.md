# 02. RAG 核心運作架構：檢索、增強與生成

- **Source Type**: 系統架構文件（Ingest #2）
- **對應簡報頁數**: Slide 3、Slide 4

## 核心定義
**RAG（Retrieval-Augmented Generation，檢索增強生成）** 是一種結合「外部知識庫搜尋」與「大型語言模型生成」的架構，讓 AI 在回答問題前先查閱指定資料。

## 兩大運作階段
1. **離線索引階段（Indexing Pipeline）**：
   - 載入文件 $\rightarrow$ 切分成段落（Chunking） $\rightarrow$ 轉換為向量（Embedding） $\rightarrow$ 存入向量資料庫。
2. **線上問答階段（Retrieval & Generation）**：
   - **Retrieve（檢索）**：將使用者問題轉為向量，從資料庫撈出最相關的 $K$ 筆資料。
   - **Augment（增強）**：把「原始問題 ＋ 檢索到的參考段落」組裝成新的 Prompt。
   - **Generate（生成）**：LLM 嚴格依據參考段落生成有憑有據的回答。

## 教學轉化提示
可將 RAG 比喻為**「允許攜帶參考資料的開書考（Open-book Exam）」**，大幅降低胡說八道的機率。
