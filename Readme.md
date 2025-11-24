# Abstract
This project aims to develop an intelligent, automated system for evaluating Qur’anic recitation with a focus on **Tajweed rule correctness**, providing students with objective, immediate, and personalized feedback. Traditional Tajweed learning requires continuous supervision from qualified sheikhs, limiting accessibility and slowing down progress—especially for beginners and remote learners. Our system addresses this gap by combining **deep learning**, **signal processing**, and **information systems design** to build a scalable digital learning platform.
The scope of the project includes:

1. **Automatic detection and evaluation of selected Tajweed rules**—specifically _Al-Mad_, _Ghunnah_, and _Ikhfaa_.
    
2. **A structured client–server model**, including a database-backed platform that manages students, sheikhs, sessions, payments, evaluations, and recitation records.
    
3. **Integration of AI evaluation into real user workflows**, where students submit recitations, the model processes them, and sheikhs can later review or override feedback.
    

The methodology begins with **collecting and preprocessing Qur’anic audio samples** using the QDAT dataset. Audio recordings are transformed into **normalized mel-spectrograms**, enabling visual feature extraction using convolutional neural networks. An enhanced **EfficientNet-B0 architecture with Squeeze-and-Excitation (SE) attention blocks** is used to classify and evaluate the correctness of targeted Tajweed rules. The model is trained, validated, and compared against existing benchmarks using accuracy, confusion matrices, and reliability metrics. For the platform layer, a normalized **relational database schema** is designed with strong constraints, integrity rules, and secure handling of user roles (student, sheikh, admin), payment operations, and session workflows. RESTful APIs are used for interaction with the frontend.

Results show that the system achieves **high accuracy across all rules**, surpassing previously published scores, proving the effectiveness of mel-spectrogram–based deep learning for Tajweed evaluation. The platform design ensures scalability, security against SQL injection, complete entity–relationship modeling, and support for real structured learning cycles between students and sheikhs.

This project demonstrates a practical path toward **AI-assisted Qur’an education**, bridging traditional learning with modern technology. It offers a unified framework combining machine learning, database systems, and user experience design—ultimately enabling real-time, accessible, and standardized Tajweed evaluation for learners worldwide.
