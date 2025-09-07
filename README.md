# NowvaAI

Intelligent motion analysis and real-time feedback for resistance training, using computer vision and knowledge-driven AI.
This repository contains the software system powering the automated squat rack’s AI coach. The goal is to fuse pose estimation, machine learning, and symbolic reasoning into a unified framework capable of delivering real-time, biomechanically grounded feedback to athletes.
🔬 System Overview
Multi-Camera Pose Estimation
Multi-view capture with stereo calibration and triangulation.
Extraction of 2D/3D joint landmarks using MediaPipe/OpenPose.
Feature Engineering
Temporal joint angle sequences (knee, hip, ankle, spine).
Derived kinematic metrics (velocity, ROM, symmetry, stability).
ML/DL Models for Motion Classification
LSTM / Transformer networks for sequential motion analysis.
Alternative gradient-boosted trees (XGBoost) for rep-level classification.
Models trained on curated squat datasets (good vs. faulty reps).
AI Coaching Agent
Knowledge graphs & trees encoding exercise principles, error taxonomies, and corrective cues.
Retrieval-Augmented Generation (RAG) for context-aware, explainable feedback.
Real-time inference loop linking pose → features → classification → feedback.
Continuous Improvement
Dataset expansion through human-in-the-loop annotation.
Offline fine-tuning of pose models for improved robustness to gym-specific conditions.
Modular architecture for extending to other lifts (bench, deadlift, OHP).
🎯 Research Goals
Evaluate the trade-offs between sequential deep models (LSTM/Transformer) and classical methods (XGBoost) for rep classification.
Explore integration of symbolic reasoning (graphs, knowledge trees) with statistical ML for coaching.
Achieve sub-200 ms end-to-end latency for real-time corrective feedback.
Establish a scalable pipeline for multi-lift expansion.
This system aims to serve as a hybrid AI coach: combining data-driven recognition of movement with structured, explainable feedback grounded in exercise science.
