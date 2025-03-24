# RAG

## Introduction

RAG（Retrieval-Augmented Generation）系統是一種結合檢索與生成技術的模型架構，主要用於提高文本生成的準確性與知識豐富度

### System Structure

<li>檢索器（Retriever）：
通常採用密集檢索或基於稀疏檢索（如TF-IDF）的方法，快速從大規模知識庫中篩選出與輸入查詢最相關的文檔或段落。
<li>生成器（Generator）：
基於預訓練的大型語言模型，如BART或GPT，生成器根據檢索到的上下文信息來生成回答或文本內容，從而保證生成內容的相關性和準確性。

### Advantages

<li>知識豐富：由於檢索模塊能夠及時獲取外部資訊，RAG系統在回答問題或生成內容時能夠提供更多背景知識，減少生成虛假信息（hallucination）的可能性。
<li>動態更新：當知識庫更新時，RAG系統能夠自動利用最新的信息，而不需要重新訓練整個生成模型，這對於應對不斷變化的知識環境非常有用。
<li>靈活應用：該架構廣泛應用於開放域問答、文本摘要、對話系統等多種NLP任務中，提升了系統在特定領域中的專業性和準確性。

## Equipment, IDE

<li>Apple Sillicon M1 Pro
<li>Visual Studio Code

## Environment Setup

1. Create conda environment
2. Download some requirements

```bash
pip install -r requirements.txt
```

3. Type the follow command, then enter the huggingface token <a urls="https://huggingface.co/docs/hub/security-tokens">Apply Token</a>

```bash
huggingface-cli login
```
