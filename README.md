# Benchmarking LLMs on Checkers

A comparative evaluation of reasoning and rule compliance across 
three large language models using the game of Checkers as a benchmark.

## Models Tested
- LLaMA 3.2 3B (Meta AI)
- Mistral 7B (Mistral AI)
- Qwen 2.5 7B (Alibaba Cloud)

## Key Results

| Model        | Win Rate | Illegal Moves | Avg Captures |
|--------------|----------|---------------|--------------|
| LLaMA 3.2 3B | 30%      | 23            | 10.1         |
| Mistral 7B   | 40%      | 43            | 9.6          |
| Qwen 2.5 7B  | 20%      | 4             | 9.1          |

## How to Run

The notebook runs on Google Colab with a free GPU via Ollama 
for fully local model inference.

### Step 1 — Open in Colab
Upload `checkers_benchmark.ipynb` to Google Colab and enable 
GPU under Runtime → Change runtime type → T4 GPU.

### Step 2 — Install Ollama and Pull Models
The first cell of the notebook installs Ollama automatically. 
Models are not included in this repository due to their size 
(2 to 5 GB each). You have two options:

**Option A — Pull models fresh every session (recommended)**

The notebook will download them automatically when you run 
Cell 1. This requires a stable internet connection and takes 
roughly 10 to 15 minutes the first time.

**Option B — Save models to your own Google Drive**

If you want to avoid re-downloading every session, follow 
the instructions in Cell 1 of the notebook to save the models 
to your own Google Drive for reuse.

### Step 3 — Mount Google Drive
Cell 2 mounts Google Drive to save results. Make sure you 
are signed in to your Google account when the permission 
popup appears.

### Step 4 — Run All Cells
Run all cells in order. Results are saved automatically to 
Google Drive after every game so no progress is lost if 
the session disconnects.



## Repository Structure
- `checkers.ipynb` — full benchmark notebook
- `checkers.py` — full benchmark python file
- `checkers_benchmark.pdf` — static view of notebook with outputs
- `results/` — game results in JSON format (20 games per model)
- `charts/` — all visualisation charts
- `LLM_Checkers_Simple_Presentation_v2.pptx` — project presentation

## Course
AI and Project Work — University of Bologna (Erasmus)  
TU Dortmund, M.Sc. Data Science

