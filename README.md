# **CBIR with Near Duplicate Detection using CLIP and Fusion Models**  

This repository contains the implementation of a project focused on **Content-Based Image Retrieval (CBIR)** with near duplicate detection in the domain of radiology. It explores multimodal learning with **CLIP** and incorporates a **fusion network** for combined image and text embeddings.  

---

## **Project Overview**  

### **Objectives**  
- Train and fine-tune a **CLIP** model on the ROCO (Radiology Objects in Context) dataset.  
- Perform **near duplicate detection** using cosine similarity between embeddings.  
- Experiment with fusion models for combining image and text embeddings.  
- Evaluate the effectiveness of the approach for CBIR tasks without ground truth labels.  

### **Key Features**  
- Multimodal image-text embedding learning with CLIP.  
- Fusion network for combined embeddings.  
- Custom similarity spreading technique to enhance detection precision.  
- Manual evaluation for selected pairs.  

This work was conducted as part of a research project at **Université Paris Cité**, supervised by **Camille Kurtz**.  

---

## **Dataset**  

**ROCO (Radiology Objects in Context)**  
- Dataset of radiology images with associated textual descriptions.  
- Train-validation-test split: **80%-10%-10%.**  
- Subset used: **1,000 samples** for fine-tuning experiments.  

---

## **Implementation Details**  

### **Method 1: CLIP Fine-Tuning**  
- Fine-tuned CLIP on the ROCO dataset for **10 epochs**.  

### **Method 2: Fusion Network**  
- Combined image and text embeddings using a **learnable fusion layer**.  
- Fully connected layer to reduce embedding dimensionality (e.g., 1024 → 512).  
- Outputs normalized fused embeddings for similarity calculation.  

### **Similarity Spreading**  
- Adjusted similarity values using a custom function to enhance detection sensitivity for near duplicates.

