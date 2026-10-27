# 📘 **FinGPT and FinBERT Demo Notebooks**
This folder contains notebooks that demonstrate of several use cases of **FinGPT** and FinBERT, large language model designed for financial applications. 

> ⚠️ **Important:** Before running their cells, please make sure to follow any setup instructions provided below (eg. API keys, runtime settings). It will take about an hour to do all the setup.

Detailed instructions are in each individual notebook.
1. Set up an access token on HuggingFace and write down its value.
2. Consider getting a Colab Pro subscription to enable the L4 and/or A100 runtime. Otherwise, you will be limited to a T4 GPU whose VRAM is insufficient for many models here.
3. Get a SEC API Key
4. Get an FMP API Key.

> **FinGPT GitHub repository**: [FinGPT GitHub](https://github.com/AI4Finance-Foundation/FinGPT). The FinGPT notebooks are based on the open-source work by the **AI4Finance Foundation**.
> **FinBERT GitHub repository**: [FinBERT GitHub](https://github.com/ProsusAI/finBERT)
---

# Notebook Status
Because these notebooks are typically run in Google Colab, the packages they are run with can change as they are updated in Google Colab runtimes. So, important to debug this periodially.
1. Reproduce Benchmark OS: worked August 13
2. Analyze financial reports OS: worked August 31
3. Sentiment Analysis OS: worked August 13
4. Multi-task financial LLMs Models OS: worked September 1
5. FinGPT_Forecaster OS: worked September 1
6. FinBERTManyUseCases: ...
---


### FinGPT Benchmark Reproduction
This part is used to reproduce the result of performance of the **FinGPT v3.2** sentiment classification models on four different financial sentiment analysis datasets.

**Benchmark Results (expected results):**  

||[Financial_Phrasebank(FPB)](https://huggingface.co/datasets/takala/financial_phrasebank)|[FiQA SA](https://huggingface.co/datasets/pauri32/fiqa-2018)|[Twitter Financial News Sentiment (TFNS)](https://huggingface.co/datasets/zeroshot/twitter-financial-news-sentiment)|[News With GPT Instruction (NWGI)](https://huggingface.co/datasets/oliverwang15/news_with_gpt_instructions)|  
|-----|-----|-----|-----|-----|
|Weighted F1|0.850|0.860|0.894|0.632|  
|ACC/F1 Micro|0.851|0.844|0.894|0.636|  
|Macro F1|0.840|0.752|0.866|0.644|

📌 Use this notebook to reproduce the benchmark results: [Reproduce Benchmark.ipynb](./1Reproduce_Benchmark.ipynb)

---

### FinGPT and Analyzing Financial Reports
This notebook is to analyze financial reports, particularly annual reports (10-K), using large language models, and to generate comprehensive PDF reports that provide insights into a company’s financial health and performance over the fiscal year.

📌 Use this notebook to analyze financial reports: [Analyze financial reports.ipynb](./2Analyze_financial_reports_ollama.ipynb)

---

### FinGPT and Sentiment Analysis
This notebook demonstrates how to load a LLaMA2-based FinGPT sentiment analysis model and generate sentiment predictions for financial news prompts.

📌 Use this notebook to run the sentiment analysis demo: [Sentiment Analysis.ipynb](./3Sentiment_Analysis.ipynb)

>If you want to train your own model, please refer to this FinGPT notebook:
[FinGPT Training LoRA with ChatGLM2 6B for Beginners](https://github.com/AI4Finance-Foundation/FinGPT/blob/master/FinGPT_Training_LoRA_with_ChatGLM2_6B_for_Beginners_v2-2.ipynb)

---

### FinGPT and Multi-task Financial LLMs
This notebook demonstrates the multi-task capabilities of FinGPT's financial language models. The supported tasks include:

- Financial Sentiment Analysis
- Headline Classification
- Named Entity Recognition
- Financial Relation Extraction

📌 Use this notebook to explore multi-task financial LLM models: [Multi-task financial LLMs Models.ipynb](./4Multi_task_financial_LLMs_Models.ipynb)

---

### FinGPT and Forecasting
This section demonstrates how to use the FinGPT forecasting pipeline to predict stock price movements using historical price and sentiment data. It is adapted from the official FinGPT forecasting demo notebook.

📌 Use this notebook to run the FinGPT forecasting demo: [FinGPT Forecaster.ipynb](./5FinGPT_Forecaster.ipynb)

---

### FinBERT and its Many Use Cases
This section demonstrates how to use the FinBERT for many, many things.

📌 Use this notebook to run the FinBERT demos: [FinBERTManyUseCases.ipynb](./FinBERTManyUseCases.ipynb)



