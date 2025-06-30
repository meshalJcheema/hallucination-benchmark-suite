# 🧠 Benchmarking Hallucination-Detection Frameworks

This repository provides a **complete, notebook-driven workflow** for building, hallucinating, and stress-testing QA datasets—then benchmarking multiple hallucination-detection frameworks against them.  
Whether you’re validating a single LLM or comparing entire toolchains, these notebooks give you a reproducible pipeline from raw corpus ➜ hallucinated examples ➜ detection metrics & leaderboards.

---

## 📂 Project Structure

| Path | Purpose |
| ---- | ------- |
| `dataset_preparation.ipynb` | Builds a **ground-truth QA set** from RAGBench-COVIDQA (or any corpus) & stores it in a unified JSON/Parquet format. |
| `generate_hallucinated_dataset.ipynb` | Uses prompting + filtering to **inject controlled hallucinations** into a subset of the QA pairs, tagging each instance with “truthful” / “hallucinated”. |
| `benchmarking_hallucination_detection_frameworks.ipynb` | Orchestrates multiple detection libraries / models (OpenAI, Groq, UpTrain, TruthLLM …) on the mixed dataset & logs raw outputs. |
| `Evaluate_Hallucination_Detection_Frameworks_Performance.ipynb` | Computes precision, recall, F1, ROC-AUC, and cost metrics, then generates comparative plots & a Markdown leaderboard. |

