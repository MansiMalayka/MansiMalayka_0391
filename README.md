![image](https://github.com/user-attachments/assets/02ed40c9-54ff-475f-8435-2403405f3d53)

This project involves developing a speech-to-text translation system that processes audio inputs in English, transcribes them, and then translates the transcriptions into Gujarati. The model’s purpose is to support individuals requiring translations of spoken English content into Gujarati, enhancing accessibility and understanding for Gujarati speakers. The project uses deep learning and natural language processing (NLP) techniques, including audio preprocessing, language modeling, and translation.

Project Workflow
The project consists of three primary stages:

Data Preparation: Processing the raw audio files and associated transcriptions to ensure clean, normalized inputs.
Model Training: Utilizing models for speech-to-text transcription in English and translating the output into Gujarati.
Evaluation and Testing: Measuring model performance on unseen data to ensure accuracy and efficiency.
Step-by-Step Implementation
1. Data Preparation
Objective: Clean, organize, and prepare data for training, validation, and testing.
Input Data: A CSV file containing columns for the audio file paths, English sentences, and their corresponding translations in Gujarati. Additionally, a folder with the raw audio files.
Processing Steps:
Preprocessing Audio: The audio data is normalized to standard formats and sampling rates, ensuring consistent quality and length.
Splitting Data: The dataset is split into training, validation, and test sets using an 80/10/10 ratio. This partitioning allows for model training, hyperparameter tuning, and evaluation on separate datasets.
2. Model Development
Architecture Choice: The VITS (Variational Inference Text-to-Speech) model is used, as it supports efficient speech synthesis and transcription tasks.
Modules and Libraries:
Torch: For building and training deep learning models.
VITS Library: The VITS model has modules for text and audio processing, making it suitable for this task.
Commons, Utils, and Train Functions: Core functions from the VITS library to load data, preprocess it, and perform training.
Training Process:
The model is trained to transcribe English audio inputs accurately. After training, the model takes spoken English audio, transcribes it to text, and generates corresponding translations.
Fine-Tuning: The model is fine-tuned with the validation dataset to improve accuracy and prevent overfitting.
3. Error Rectification and Dependencies
Module Errors: During development, several errors related to module imports were encountered, including missing dependencies like unidecode. These were resolved by installing the necessary packages.
File Handling: Adjustments in file paths and data handling scripts were made to ensure the model could access the required data and save output in the correct format.
4. Translation
The English transcription output is then translated into Gujarati using NLP translation models or APIs. This step completes the end-to-end pipeline from audio input to Gujarati translation output.
Model Evaluation
To ensure accuracy, the model’s performance was evaluated on the test dataset, focusing on:

Transcription Accuracy: How well the model transcribed spoken English.
Translation Quality: Accuracy and fluency of the Gujarati translation output.
