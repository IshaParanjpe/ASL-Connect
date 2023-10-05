# ASL Connect: Bridging Communication Gaps with Machine Learning and ASL

## Overview
ASL Connect is an innovative project that utilizes Machine Learning, Computer Vision, and Natural Language Processing (NLP) to enable communication between individuals who are deaf or hard of hearing and those who are not proficient in American Sign Language (ASL).

## Installation

### Clone the Repository
To begin, clone the ASL Connect repository to your local machine:

```bash
git clone [repository_url]
cd ASL-Connect
```

### Install Dependencies
Install the necessary Python packages using pip:

```bash
pip install -r requirements.txt
```

### Unzip the Pre-trained Model
Unzip the pre-trained random forest model:

```bash
unzip rf_model.zip
```

### Set up IBM Watson Text-to-Speech
To use the Text-to-Speech feature, you'll need an API key and service URL from IBM Watson. Create an IBM Cloud account, generate an API key, and update the `apikey` and `url` variables in the code with your credentials.

## Usage

### Running the ASL Classifier
Execute the main ASL classifier script:

```bash
python asl.py
```

### Real-time ASL Sign Recognition
1. Point at your webcam with ASL gestures and the system will detect and classify them in real-time.

2. The classifier uses a pre-trained random forest model (`rf_model.joblib`) to predict ASL letters based on hand landmarks detected in the video.

3. ASL signs are recognized and displayed on the screen.

### Sentence Correction
1. The project corrects the interpreted sentence for improved accuracy using WordNet from the NLTK library.

2. It tokenizes the sentence and, for each word, finds its synsets (sets of synonyms).

3. If synsets are available, it replaces the word with the first lemma (synonym) found to create a more accurate sentence.

### Text-to-Speech Conversion
1. The recognized ASL signs are concatenated to form a sentence.

2. This sentence is converted into spoken language using IBM Watson's Text-to-Speech API.

3. The synthesized audio is saved to an output file (`output.mp3`).

4. The audio file is played using the "playsound" library, allowing the user to hear the spoken sentence.

## Key Features

### Real-time ASL Sign Recognition
- Utilizes the Mediapipe library for hand landmark detection.
- Classifies ASL signs based on detected landmarks using a pre-trained random forest model.

### Sentence Correction
- Improves sentence accuracy using WordNet from the NLTK library.
- Replaces recognized words with their synonyms when available.

### Text-to-Speech Conversion
- Converts the recognized ASL signs into spoken language using IBM Watson's Text-to-Speech API.
- Provides an audio output for seamless communication.

## Technologies Used

### Python
- Primary programming language for the project.

### Machine Learning
- Utilizes a pre-trained random forest model for ASL sign classification.

### Computer Vision (Mediapipe)
- Detects hand landmarks in real-time video frames.

### Natural Language Processing (NLTK)
- Implements sentence correction using WordNet and tokenization.

### IBM Watson Text-to-Speech API
- Converts recognized ASL signs into spoken language.

## License
This project is licensed under the [MIT License](LICENSE).
