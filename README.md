# EYES ON THE ROAD: STATE-OF-THE-ART VIDEO QUESTION ANSWERING MODELS ASSESSMENT FOR TRAFFIC MONITORING TASKS

---

## Introduction

This project evaluates the capabilities of five state-of-the-art (SOTA) Video Question Answering (VideoQA) models in addressing traffic monitoring challenges. The study focuses on their performance across different traffic scenarios, assessing their ability to answer questions of varying complexity.

## Table of Contents

- [Introduction](#introduction)
- [Video Sequences](#video-sequences)
- [Question Generation](#question-generation)
- [Models Used](#models-used)
- [Usage Instructions](#usage-instructions)
- [Dependencies](#dependencies)
- [Acknowledgments](#acknowledgments)

---

## Video Sequences

The study evaluates three distinct video sequences that simulate real-world traffic monitoring scenarios:

1. **Sequence 1**: Real-world scenario featuring a cyclist interacting with traffic.
2. **Sequence 2**: Real-world scene of vehicles turning onto a bike lane.
3. **Sequence 3**: Simulated intersection scenario generated using CARLA, focusing on pedestrian and vehicle interactions.

Each sequence tests the models' abilities to answer easy, moderate, and complex questions.

## Question Generation

The questions used in the evaluation were carefully designed to test various aspects of the models, such as:

- **Basic Observations**: Identifying objects or simple features in the scene.
- **Moderate Questioning**: Analyzing the relationships and dynamics between objects.
- **Complex Reasoning**: Interpreting behaviors, safety impacts, and design improvements.

These questions ensure a comprehensive evaluation of the models' capabilities.

## Models Used
- LLaVA-NeXT-Video-7B-hf
- InternVL
-  VideoLLAMA2
-  ChatGPT-4o
-  Gemini Pro 1.5



## Usage Instructions

To replicate the experiments:

1. **Prepare the Environment**: Install all dependencies listed below.
2. **Download the Video Sequences**: Ensure you have access to the required video files.
3. **Run the Models**: Use the provided scripts to evaluate each model.
4. **Analyze the Results**: Compare the model outputs with the provided question sets.

## Dependencies

- Python 3.12.4
- PyTorch
- Hugging Face Transformers
- OpenAI API
- Gemini API


## Acknowledgments

We extend our gratitude to the developers of the VideoQA as mentioned above models used in this study and the contributors for open-sourcing them and providing them with APIs.

---
