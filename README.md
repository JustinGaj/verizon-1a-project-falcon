# Project Falcon 🦅  
**Bird & Nest Detection on Cell Towers using YOLOv8**  

## 📌 Project Description  
Project Falcon uses machine learning and image analysis to detect the presence of birds and bird nests on cell towers. This work supports avian wildlife protection and ensures regulatory compliance for Verizon’s infrastructure.  

The objectives are to:  
- Detect birds and nests on cell towers with high accuracy.  
- Classify bird species where possible.  
- Provide actionable insights for tower maintenance and environmental protection.  

The system will automatically flag potential nesting sites, enabling proactive conservation measures.  

## ⚡ Model  
We use YOLOv8 (You Only Look Once), a state-of-the-art real-time object detection model known for its speed, accuracy, and efficiency, making it well-suited for bird and nest detection tasks.  

## 🗂️ Datasets  
Our project leverages multiple datasets, merged and standardized into YOLOv8 format:  
- [Roboflow: bird-nest-dataset-kpvdq](https://universe.roboflow.com/datasets-wgkry/bird-nest-dataset-kpvdq/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true)  
- [Hugging Face: JotDe/birds](https://huggingface.co/datasets/JotDe/birds)  
- [Hugging Face: Francesco/cell-towers](https://huggingface.co/datasets/Francesco/cell-towers)  
- [Hugging Face: Ez-Clap/bird-species](https://huggingface.co/datasets/Ez-Clap/bird-species)  

These datasets are cleaned, unified, and augmented to ensure diversity, robustness, and high-quality training data.  

## 🔧 Data Preparation  
- **Annotation Conversion:** All datasets converted to YOLOv8 `.txt` format.  
- **Class Standardization:** Unified into two main classes: `bird` and `nest`.  
- **Data Augmentation:** Horizontal flips, small rotations, brightness/contrast adjustments, and YOLOv8 mosaic augmentation to improve robustness.  
- **Dataset Splitting:** Train (80%), Validation (10%), Test (10%).  

## 🚀 Expected Outcome  
An automated detection system capable of:  
- Identifying birds and nests on cell towers.  
- Assisting tower maintenance teams with early warnings.  
- Supporting wildlife conservation and regulatory compliance.  
