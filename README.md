<div align="center">
  <h1>🩺 Multi‑Modal Medical Diagnosis Assistant</h1>
  <p><strong>AI-powered tool that combines imaging analysis, symptom input, and medical literature retrieval to suggest diagnoses.</strong></p>
</div>

## 🚀 Overview
The **Multi‑Modal Medical Diagnosis Assistant** processes medical images (X‑ray, MRI, CT) alongside patient symptoms and history, and provides probable diagnoses with confidence scores and literature references.

![Dashboard Demo](/C:/Users/hp/.gemini/antigravity-ide/brain/fdf49048-b37f-4711-af04-f256131d4933/medical_dashboard_placeholder.png)

## ✨ Features
- **Image Analysis:** Uses MedCLIP / Vision Transformer for feature extraction.
- **Symptom Form:** Structured input for patient-reported symptoms.
- **RAG Retrieval:** Searches PubMed abstracts to ground suggestions.
- **Explainability:** Grad‑CAM heatmaps over the uploaded image.
- **Confidence Scoring:** Top‑5 diagnoses with percentages.

## 🛠️ Tech Stack
- **Frontend:** Streamlit
- **Vision Model:** MedCLIP (ViT) fine‑tuned on CheXpert
- **LLM:** Llama‑3‑8B for reasoning
- **Vector DB:** FAISS over PubMed abstracts
- **Explainability:** Grad‑CAM visual overlays

## 📦 Installation & Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/Muhammad08-dot/multi-modal-medical-diagnosis.git
   cd multi-modal-medical-diagnosis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the app:
   ```bash
   streamlit run streamlit_app.py
   ```

## 📄 License
MIT License.
