# 🧠 LLM Wiki：RAG（檢索增強生成）核心原理與實務

> **建立方式**：採用「先討論知識骨架、再逐篇 Ingest 外部技術文章與筆記」的方式建構，作為後續自動生成教學簡報的唯一可信知識來源（Single Source of Truth）。

## 📌 知識庫討論大綱（先討論、後生成）
在匯入資料前，先與 LLM 討論初學者理解 RAG 所需的五個核心認知階梯：
1. **痛點建立**：為什麼不能只靠純 LLM？（幻覺與知識截止問題）
2. **整體輪廓**：RAG 如何用「開書考」的概念解決痛點？
3. **資料前處理**：非結構化文字如何透過 Chunking 與 Embedding 轉成向量？
4. **檢索機制**：向量資料庫（如 FAISS）如何快速找出最相關的 Top-K 段落？
5. **品質把關**：實作 RAG 時最常出錯的環節與評估指標。

## 📂 已 Ingest 知識條目清單（共 5 篇）
- [01. 為什麼需要 RAG？LLM 的幻覺與知識限制](./01-llm-hallucination.md)
- [02. RAG 核心運作架構：檢索、增強與生成](./02-rag-architecture.md)
- [03. 文件切塊（Chunking）與向量嵌入（Embedding）](./03-chunking-embedding.md)
- [04. 向量資料庫與 Top-K 相似度檢索機制](./04-vector-db-retrieval.md)
- [05. RAG 常見地雷與品質評估指標](./05-rag-evaluation-pitfalls.md)
