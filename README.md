# EYES ON THE ROAD: State-of-the-art Video Question Answering Models Assessment for Traffic Monitoring Tasks

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

## Question Generation Prompt:
```bash
You are an expert in linguistics, logic, and traffic engineering, tasked with creating questions based
on three given traffic scenarios. The questions will assess understanding at different difficulty levels, focusing on spatial
and temporal aspects. The questions will be categorized as follows:
• Easy: Questions that focus on straightforward observations (e.g., "How many cars can you see?").
• Moderate: Questions requiring attention to detail or basic reasoning (e.g., "Is the cyclist following the bike
lane?").
• Hard: Questions involving detailed analysis or traffic engineering knowledge (e.g., "What impact does the
pedestrian’s position have on vehicle flow?").
Output Requirements:
• The result should be in JSON format.
• Each question must have a unique ID.
• Generate 10 questions for each category (30 questions in total).
Scenario Details:
Provide the scenario details here.
Busy Intersection
Situation: A cyclist is on the wrong side of the road. In the video, the cyclist zips through the intersection without
stopping, creating a potential traffic hazard.
Questions Curated:
• Easy:
– Is the video taken in daylight or at night?
– How many cyclists are there?
– How many cars are there?
• Moderate:
– Is the cyclist following the bike lane?
• Hard:
– Are there any visible landmarks?
– Between 0:08 to 0:10, how many cars are moving?
Question Requirements:
• Easy: Questions should be simple and basic, focusing on straightforward observations.
• Moderate: Questions should require some attention to detail or involve interpreting specific behaviours or
interactions.
• Hard: Questions should involve advanced reasoning, detailed analysis, or traffic engineering knowledge, with
timestamps implied but not explicitly stated.
Note: Do not generate the answers.

```
## Evaluation Judge Prompt
```bash
Create a table to compare the performance of VideoQA models on three different question sets related to traffic
monitoring conditions. For each question set:
1. Provide the ground truth for the question.
2. List the model responses.
3. Indicate whether the responses were correct (score as 1 for semantically correct and 0 for completely wrong;
no partial grading).
4. Calculate the accuracy percentage for the models as:
Accuracy (%) = Number of correct responses
Total number of responses × 100
5. Calculate the consistency precision (cP ) for the models as:
cP = Total number of questions answered correctly with all questions in the category also correct
Total number of questions with all questions answered correctly
```

## Acknowledgments

As mentioned above, we extend our gratitude to the developers of the VideoQA models used in this study and the contributors for open-sourcing them and providing them with APIs.

---
