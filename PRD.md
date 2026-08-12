# Product Requirements Document (PRD): Multi-Modal Medical Diagnosis Assistant

## 1. Overview
The **Multi-Modal Medical Diagnosis Assistant** combines imaging (X‑ray, MRI) analysis, patient symptom input, and medical history to suggest possible diagnoses with confidence scores. It leverages vision transformers and a Retrieval‑Augmented Generation (RAG) pipeline on up‑to‑date medical literature.

## 2. Target Audience
- Radiologists and clinicians
- Medical AI researchers
- Hospitals looking to augment diagnostic workflow

## 3. Core Features
- **Image Analysis:** MedCLIP / BioMedCLIP for visual feature extraction.
- **Symptom & History Input:** Structured form for patient details.
- **RAG on Medical Literature:** Real‑time search over PubMed / clinical guidelines.
- **Explainability:** Grad‑CAM heatmaps and citation of supporting literature.
- **Confidence Scoring:** Probabilistic ranking of top‑5 diagnoses.

## 4. Technical Architecture
- **Frontend/UI:** Streamlit with separate tabs for Image Upload, Symptom Form, and Results.
- **Vision Model:** Pre‑trained Vision Transformer (ViT) fine‑tuned on CheXpert.
- **LLM Engine:** Llama‑3‑8B with Retrieval from a vector DB (FAISS) containing PubMed abstracts.
- **Explainability Layer:** Grad‑CAM visual overlays on uploaded images.
- **Data Privacy:** All processing occurs locally; no patient data leaves the machine.

## 5. UI/UX Design
- Dark‑mode clinical aesthetic with teal accents.
- Left panel: Image upload + quick preview.
- Right panel: Symptom entry form.
- Bottom panel: Results table with confidence, heatmap overlay, and literature links.

## 6. Development Milestones
1. **M1:** Build Streamlit scaffolding (tabs, file uploader).
2. **M2:** Integrate MedCLIP model for image feature extraction.
3. **M3:** Implement symptom form and vector‑DB retrieval pipeline.
4. **M4:** Assemble LLM prompt chain and generate diagnosis output.
5. **M5:** Add Grad‑CAM overlay and confidence visualization.
6. **M6:** Final polish, README, and deployment instructions.
