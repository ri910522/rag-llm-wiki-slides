# 03. 文件切塊（Chunking）與向量嵌入（Embedding）

- **Source Type**: 資料前處理筆記（Ingest #3）
- **對應簡報頁數**: Slide 5

## 為什麼需要切塊（Chunking）？
- 整份 PDF 或長篇食記太長，直接塞進 LLM 會超出上下文長度（Context Window）限制，也會稀釋重點。
- 常見做法是設定固定字元長度（例如 `chunk_size = 500`）並保留重疊區間（`chunk_overlap = 50`），避免句子在邊界被硬生生切斷。

## 什麼是向量嵌入（Embedding）？
- 電腦無法直接比較兩段文字的「語意」是否相近，因此需要透過 Embedding 模型（如 `SentenceTransformers` 或 `text-embedding-3`）把文字壓縮成一串高維度數字（向量）。
- **核心特性**：語意越相近的句子（例如「推薦不辣的火鍋」與「清淡豚骨鍋物」），在向量空間中的距離就越接近。
