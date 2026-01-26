Overview

Smallholder farmers in Kerala often lack timely, expert guidance for emerging crop problems. This system delivers real-time crop diagnostics and advisory by combining on-device computer vision, Malayalam conversational AI, and secure record-keeping.

Field images or videos of crops are analyzed using deep learning models—YOLOv8 for pest/object detection and EfficientNet for disease and nutrient deficiency classification. A Malayalam-speaking AI assistant allows farmers to ask questions via voice or text and receive contextual, locally relevant recommendations.

To ensure reliability in rural environments, core models are deployed using TensorFlow Lite for offline edge inference on smartphones or low-cost devices. All diagnoses and advisory interactions are logged on a tamper-proof blockchain ledger, ensuring transparency, trust, and auditability.

Key Features

YOLOv8-Based Object Detection
Detects pests, weeds, insects, rodents, and crop anomalies in real time

Optimized lightweight variants reduce model size while maintaining high accuracy

Suitable for live camera feeds, traps, or drone imagery

EfficientNet-Based Disease Classification
Identifies plant diseases and nutrient deficiencies from leaf images

High accuracy with low latency, enabling fast on-device inference

Compact model size suitable for mobile deployment

Malayalam Conversational AI
Supports voice and text interaction in Malayalam and English

Enables farmers to ask natural questions such as:

“What disease is affecting my pepper leaves?”

“What spray should I apply now?”

Uses speech recognition and text-to-speech models trained on Malayalam corpora

Blockchain-Backed Logging
Every diagnosis and recommendation is logged immutably

Enables transparent record-keeping for:

Crop insurance claims

Audits and certifications

Historical farm analysis

Offline TensorFlow Lite Inference
Core vision and speech models run fully on-device

Ensures functionality in low or no-connectivity environments

Delivers sub-second diagnostics without cloud dependency

Split Edge–Cloud Architecture
Edge: Image capture, vision inference, speech processing

Cloud: Reasoning engine, advisory synthesis, data aggregation

Minimizes bandwidth usage by transmitting only compact summaries

System Architecture

Edge Devices (smartphones, tablets, IoT cameras):

Capture crop images or video

Run YOLOv8 and EfficientNet TFLite models locally

Handle Malayalam ASR/TTS for user interaction

Cloud Backend:

Combines vision outputs with weather, soil, and historical data

Executes the reasoning engine for personalized advisory

Synchronizes blockchain logs when connectivity is available

This modular, fault-tolerant design ensures fast diagnostics, secure data handling, and scalable deployment across rural settings.

Machine Learning Models Used

YOLOv8 – Object detection for pests, weeds, and field anomalies

EfficientNet (B0/B3) – Plant disease and nutrient deficiency classification

Malayalam ASR/TTS Models – Voice-based farmer interaction

NLU Module – Intent and entity extraction from farmer queries

Reasoning Engine – Rule-based and contextual advisory generation

Blockchain Smart Contract – Immutable diagnostic and advisory logging

Performance Highlights

High Accuracy

Pest and object detection accuracy exceeding 90%

Disease classification accuracy close to 99% on benchmark datasets

Low Latency

Image classification in ~60–70 ms per frame

Real-time video processing on edge hardware

Compact Model Size

EfficientNet TFLite ~15 MB

Optimized YOLO variants significantly reduce parameter count

Low Bandwidth Usage

Only alerts, summaries, and logs are transmitted

Fully functional even on limited 3G connectivity

Getting Started Prerequisites

Python 3.8+

TensorFlow / TensorFlow Lite

PyTorch (for training)

Node.js or Go (for blockchain components) Datasets Used

Plant Disease Images: Large-scale labeled leaf disease datasets

Kerala Field Data: Locally collected images of rice, coconut, banana, pepper, etc.

Pest & Weed Data: Public and field-captured insect and weed images

Malayalam Speech Data: Open-source Malayalam speech corpora

Auxiliary Data: Weather, soil, and market price datasets

Applications

Early Pest & Disease Detection

Personalized Spray and Fertilizer Scheduling

Localized Agricultural Advisory in Malayalam

Traceable Farm Record Management

Support for Crop Insurance and Certification
