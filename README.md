# Automated-Chest-X-ray-Diagnosis-Report-Generation
## Project Overview
This project is an end-to-end medical imaging solution designed to classify pathologies from Chest X-rays and generate preliminary diagnostic insights. It leverages Deep Learning to assist radiologists by providing automated screenings, aiming for high interpretability and clinical viability.
## Tech Stack & Rationale
### Deep Learning: CNN (Convolutional Neural Networks)
- Why: CNNs are the industry standard for computer vision, capable of identifying subtle spatial patterns in X-ray images that dense layers might miss.
### Backend: Flask REST API
- Why: Chosen for its lightweight footprint, allowing for fast model inference serving without the overhead of heavier frameworks.
### Infrastructure & DevOps: Docker & AWS EC2
- Why: Docker ensures the environment is reproducible. AWS EC2 provides the scalable compute power necessary for GPU/CPU intensive model hosting.
### Storage: AWS S3
- Why: S3 provides a highly available and durable repository for storing massive medical image datasets and model weights.
## System Architecture
1. Data Ingestion: Images are uploaded/stored in AWS S3.
2. Preprocessing: Normalization and resizing of X-ray images for model compatibility.
3. Inference: The CNN-based classifier processes the image to output diagnostic probabilities.
4. API Layer: A containerized Flask API receives requests and returns JSON responses containing classification results.
5. Deployment: Hosted on AWS EC2 for cloud-accessible inference.
## Performance & Evaluation
The system was evaluated using rigorous clinical metrics to ensure reliability:
1. AUC-ROC: Measures the model's ability to distinguish between classes.
2. F1-Score: Balances precision and recall, crucial for medical diagnosis where false negatives are costly.
3. Sensitivity & Specificity: Ensures the model is accurate in identifying both the presence and absence of disease.
## Author
### Shreyas Deshpande
- MSc Advanced Computer Science, Oxford Brookes University
- Portfolio: [shreyasdeshpande.in](https://shreyasdeshpande.in/)
- LinkedIn: [linkedin.com/shreyasdeshpande7](https://www.linkedin.com/in/shreyasdeshpande7/)
