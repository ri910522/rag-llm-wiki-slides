# 04. 向量資料庫與 Top-K 相似度檢索機制

- **Source Type**: 檢索演算法實作筆記（Ingest #4）
- **對應簡報頁數**: Slide 6

## 向量資料庫的角色
- 專門用來儲存並快速搜尋高維度向量的資料庫，常見工具包含 **FAISS**（Meta 開源輕量級檢索庫）、Chroma 與 Pinecone。

## Top-K 檢索運作流程
1. 使用者輸入問題後，用**同一款 Embedding 模型**將問題轉成查詢向量（Query Vector）。
2. 計算查詢向量與資料庫中所有 Chunk 向量的**餘弦相似度（Cosine Similarity）**。
3. 依照分數由高到低排序，取出前 $K$ 筆（例如 `Top-3`）最相關的段落送給 LLM。
