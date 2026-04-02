# Kaplan-Martinez-ITAI1378
Computer Vision Course
-
MidTerm ReadMe File:
Project Overview:
Kaplan Martinez as the Project Manager; Tier level 2
PackageGuard AI is a computer vision solution designed to automate the quality control process in logistics and warehouse environments. By utilizing Deep Learning, this system identifies structural damage in packages (cracks, tears, moisture, or crushing) in real-time as they move across a conveyor belt.

The Problem:
In high-volume distribution centers, manual inspection for package damage is:

Slow - Reducing the throughput of the facility.

Error-Prone - Human inspectors often miss subtle damage due to fatigue.

Costly - Undetected damage leads to expensive insurance disputes and customer dissatisfaction.

The Solution:
A binary classification system powered by a Convolutional Neural Network (CNN) that categorizes images as either "Intact" or "Damaged". This allows for automated flagging and diversion of compromised goods before they leave the facility.

Technical Architecture:
This project builds upon the foundational concepts of Computer Vision explored in my previous research;

Classical Machine Learning (SVM) - Evaluated for simple feature extraction.

Multi-Layer Perceptrons (MLP) - Tested for basic neural network classification.

Convolutional Neural Networks (CNN) - Selected as the primary architecture due to its superior ability to preserve spatial hierarchies and recognize complex textures.

Dataset Plan and Metrics:
Synthetic Oversampling - We utilize specialized augmentations (Cutout and GridMask) to simulate holes, tears, or crushing on "Intact" samples, artificially increasing the count of damaged examples.

Strategic Class Balancing - We perform a manual cleaning of the dataset to maintain a strict 50/50 ratio between damaged and healthy samples, forcing the model to learn the specific features of failure rather than simply guessing the majority class.

Normalization - All images are standardized to a 224x224 resolution and normalized for the PyTorch tensor format.

To meet the rigorous demands of the logistics industry, the model is evaluated based on:

Primary Metric - Recall (Target: ≥ 92%). It is critical that the system does not miss a damaged box, even if it occasionally flags a healthy one for manual review.

Secondary Metric - Inference Latency (Target: < 200ms). The system must process images fast enough to keep up with standard industrial conveyor speeds.

Week-by-week plan:
Phase 1: Environment setup and dataset acquisition.

Phase 2: Implementation of the Imbalance Correction pipeline.

Phase 3: CNN Model training and hyperparameter tuning.

Phase 4: Performance validation and visualization of misclassifications.

Phase 5: Final presentation and documentation.

Resources:
This will be produced using Google CoLab and PyTorch with zero cost.

Risk and Mitigation:
Challenge - Low-quality images in dark warehouses.

Plan B - Use a "Pre-trained" model that has already seen millions of images, making it smarter.

Challenge - Subtle damage (like a small wet spot).

Plan B - Increase image resolution or use "Image Enhancement" filters before classification.
