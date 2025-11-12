# 🧠 Teaching LLMs to See and Guide: Context-Aware Assistance in AR/VR  

This repository presents a **context-aware large language model (LLM) assistant** designed for **real-time, multimodal task guidance** in augmented and virtual reality (AR/VR) environments. 

You can access the paper here: [arXive](https://arxiv.org/abs/2511.00730)

As workers perform complex tasks, AR/VR devices capture rich multimodal data streams—including **gaze**, **hand actions**, **RGB video**, **Depth**, **dialogue history**, and etc—that can reveal user intent and task state in real time.  

Our framework integrates these diverse modalities into a unified prompting pipeline for **adaptive, real-time, and context-aware question answering**. We introduce an **incremental prompting framework** to systematically evaluate how adding contextual information improves model reasoning and response quality. Using the **[HoloAssist dataset](https://holoassist.github.io) from Microsoft Research**, we demonstrate that multimodal context significantly enhances both the accuracy and relevance of LLM-generated guidance.  

---

## 🚀 Key Features  
- 🧩 Real-time multimodal LLM assistant for AR/VR task support  
- 🖐️ Integration of real-time dialouge, hand actions, and task-step context  
- 🧠 Incremental prompting framework for controlled evaluation  
- 📊 Experiments conducted on the **HoloAssist** dataset
- 📊 Ablation studies highlighting the contribution of each contextual input
- 💬 Insights into multimodal reasoning for intelligent task guidance  

---

## 💡 Impact  
This work highlights how **LLM-driven multimodal integration** can enable **adaptive, human-centered AI systems** that transform industrial training and on-the-job assistance through AR and VR technologies.  

By bridging perception, reasoning, and action, this project contributes toward building **trustworthy and context-aware intelligent assistants** for next-generation immersive environments.  


## 🧩 How to Use  
- `Incremental Prompting Framework.ipynb`: Includes prompt templates for each model and API calls for generating responses. Requires your own endpoint and API key.  
- `Evaluation Methods.ipynb`: Implements lexical and LLM-as-a-judge evaluation. Run after responses for all four models are generated.
- `Sample Data.csv`: Provides sample data to help you reproduce results and extend the framework to other applications.

## 🧾 Citation  
If you use this work, please cite:  

**Qorbani, M., Paynabar, K., & Moghaddam, M. (2025).**  
*Teaching LLMs to See and Guide: Context-Aware Real-Time Assistance in Augmented Reality.*  
arXiv preprint arXiv:2511.00730. [https://arxiv.org/abs/2511.00730](https://arxiv.org/abs/2511.00730)

## 📬 Contact  
For questions, collaborations, or feedback, feel free to reach out:  

- **Mahya Qorbani** – [mqorbani3@gatech.edu](mailto:mqorbani3@gatech.edu)  
- **Mohsen Moghaddam** – [mohsen.moghaddam@gatech.edu](mailto:mohsen.moghaddam@gatech.edu)

