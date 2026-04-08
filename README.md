# BridgSign – Real-Time Sign Language AI

Convert text, video, or audio into fluent sign-language animations.

## The Challenge
Translating spoken/written language to sign language requires:
- Real-time video processing (30 FPS target)
- 1000+ custom motion sequences for sign units
- NLP grammar transformation (text → sign gloss)
- Seamless avatar animation with lip-sync

## How It Works
1. **Input Processing**: ASR for audio (Arabic/French), text normalization
2. **NLP Pipeline**: spaCy + Gemini API for text→gloss transformation
3. **Motion Matching**: 1000-unit sign database lookup
4. **Motion Smoothing**: Savitzky-Golay filtering + cubic-spline interpolation for 73% jitter reduction
5. **Avatar Rendering**: MediaPipe pose + forward-kinematics for finger rotations + facial blendshapes

## Results
- **30 FPS real-time playback** (target achieved)
- **73% jitter reduction** in motion sequences
- **Supports**: Tunisian, French, English Sign Language
- **Live demo**: [link]

## Tech Stack
Python, MediaPipe, OpenCV, Gemini LLM, Flask, spaCy, MongoDB, WebGL

## Important privacy note

This repository does **not** include:
- proprietary motion databases
- customer or company infrastructure
- internal extraction notebooks
- private model weights
- production deployment code
- any confidential sign assets or recordings

All included examples are synthetic, sample-based, or rewritten for public reproducibility.
