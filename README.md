# 🦅 Project Falcon  
## AI-Driven Bird & Nest Detection on Cell Towers (YOLOv8)

## 📌 Overview
**Project Falcon** is an end-to-end computer vision system developed as part of the **Verizon AI Studio Final Project**. The project applies deep learning to automatically detect **birds, bird nests, and (optionally) bird species** on cell towers using image data.

The system is designed to help telecommunications providers:
- Protect avian wildlife
- Maintain regulatory compliance with federal wildlife laws
- Reduce operational delays and inspection costs
- Improve tower maintenance planning through early, automated detection

Each year, **4–40 million bird deaths** are attributed to cell towers. Project Falcon demonstrates how AI can be used responsibly to mitigate this impact while improving operational efficiency.

---

## 🎯 Objectives
- Detect **occupied and unoccupied bird nests** on cell towers  
- Detect **birds** and optionally classify **bird species**
- Automatically flag potential nesting sites for proactive action
- Reduce reliance on manual tower inspections
- Support environmental stewardship initiatives

---

## 🧠 Model Architecture
Project Falcon uses **YOLOv8 (You Only Look Once)** — a state-of-the-art real-time object detection model optimized for:
- High detection accuracy
- Low inference latency
- Scalability across large image pipelines

### Supported Tasks
1. **Nest Detection** (Binary Object Detection)
2. **Bird Detection**
3. **Bird Species Classification** (Optional Extension)

---


## 🗂️ Datasets  
Our project leverages multiple datasets, merged and standardized into YOLOv8 format:  
- [Roboflow: bird-nest-dataset-kpvdq](https://universe.roboflow.com/datasets-wgkry/bird-nest-dataset-kpvdq/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true)  
- [Hugging Face: JotDe/birds](https://huggingface.co/datasets/JotDe/birds)  
- [Hugging Face: Francesco/cell-towers](https://huggingface.co/datasets/Francesco/cell-towers)  
- [Hugging Face: Ez-Clap/bird-species](https://huggingface.co/datasets/Ez-Clap/bird-species)  

Each dataset varied significantly in quality, annotation style, and format, requiring extensive preprocessing and validation.

---

## 🔧 Data Preparation Pipeline
A major focus of the project was **data quality and standardization**, which had a greater impact on model performance than architecture complexity.

### Key Steps
- **Annotation Conversion**  
  Converted all datasets to YOLOv8 `.txt` format
- **Class Standardization**  
  Unified labels into core classes: `bird`, `nest`, and species labels
- **Data Cleaning**  
  Removed corrupted, duplicated, blurry, and low-quality images
- **Data Augmentation**
  - Horizontal flips  
  - Small rotations  
  - Brightness & contrast adjustments  
  - YOLOv8 mosaic augmentation
- **Dataset Splitting**
  - Training: 80%  
  - Validation: 10%  
  - Test: 10%

Tools used: OpenCV, Pillow, Roboflow, Google Colab

---

## 📊 Model Evaluation & Metrics

### 🪹 Nest Detection (Binary Classification)
- **Precision:** 95.41%  
- **Recall:** 85.01%  
- **Accuracy:** 81.82%  
- **F1 Score:** 89.91%

### 🐦 Bird Detection & Species Classification
- **Top-1 Accuracy:** 75.9%  
- **Top-5 Accuracy:** 94.7%  
- **Detection Recall:** 92.8%

A **40% confidence-gating mechanism** was implemented to suppress low-confidence predictions and reduce false positives on ambiguous images (e.g., camouflage, blur).

---

## 💼 Business & Operational Impact
Project Falcon delivers measurable value across multiple dimensions:

- **Time Savings**  
  Automated detection allows maintenance scheduling around nesting cycles.

- **Legal & Regulatory Protection**  
  Accurate identification reduces the risk of violating federal wildlife laws.

- **Cost Reduction**  
  Decreases reliance on costly manual inspections and repeat site visits.

- **Operational Efficiency**  
  Enables scalable processing of thousands of image feeds.

- **Wildlife Conservation**  
  Supports conservation-aligned operations and environmental responsibility goals.

---

## 🛠️ Technologies Used
- YOLOv8 (Ultralytics)
- Python
- OpenCV
- Pillow
- Google Colab
- Roboflow
- Hugging Face Datasets
- GitHub

All tools reflect **industry-standard workflows** for scalable computer vision systems.

---

## 🚀 Future Work
Planned and proposed extensions include:
- Detecting whether a **cell tower structure** is present before wildlife detection
- Integrating **audio-based cues** for bird species classification
- Combining nest detection and species classification into a unified pipeline
- Expanding datasets with **region-specific bird species**
- Developing a **user-friendly interface** for field teams

---

## 👥 Team
Developed by a cross-university team as part of **Verizon AI Studio**:

- Justin Gajewski — Stevens Institute of Technology  
- Ayooluwa Olotu — Howard University  
- Aastha Oza — University of Houston  
- Valantina Zeremariam — Vassar College  
- Kalyn Bui — San Jose State University  
- Anahi Perez — Emory University
- Chris Dollo — University of Maryland, Baltimore County  
- Kenzy Ibrahim — George Mason University  

---

## 📄 Acknowledgments
Special thanks to the Verizon AI Studio team, mentors, and advisors for guidance and support throughout the project.
