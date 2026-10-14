# Fake News Detection Tool (VerifyAI)

## 1. Problem Statement

With the rapid growth of social media and digital platforms, fake news spreads quickly and can mislead people, create confusion, and influence public opinion.

Users often find it difficult to identify whether news is real or fake.

The objective of this project is to develop a web-based Fake News Detection Tool called VerifyAI that uses Machine Learning and Natural Language Processing (NLP) to analyze news content and classify it as REAL or FAKE. The system also provides a confidence score and important keywords to help users understand the prediction.

## 2. Team Members and Roles

**Ashank Raina – Frontend Developer**
- Designed the user interface using HTML, CSS, and JavaScript.
- Developed interactive components for entering news and displaying results.
- Ensured a responsive and user-friendly design.

**Akash Pandita – Frontend Developer**
- Assisted with UI/UX design and styling.
- Connected frontend components with backend APIs.
- Improved usability and frontend performance.

**Dishant Bhaskhar – Backend Developer**
- Developed server-side logic using Flask.
- Created REST APIs to connect the frontend with the Machine Learning model.
- Handled input validation, data processing, and errors.

**Vedant Toke – AI and NLP Developer**
- Collected and preprocessed fake and real news datasets.
- Implemented TF-IDF vectorization for text processing.
- Trained and evaluated the Multinomial Naive Bayes model.
- Worked on prediction confidence and keyword-based explanations.

## 3. Project Overview

VerifyAI is a full-stack Machine Learning web application that identifies whether a news headline or article is REAL or FAKE.

The system uses Natural Language Processing to analyze text and a supervised Machine Learning algorithm to make predictions.

**Technologies Used**
- Machine Learning: Multinomial Naive Bayes
- NLP: TF-IDF Vectorization
- Backend: Flask
- Frontend: HTML, CSS, and JavaScript

## 4. Objectives

- Detect fake news using Machine Learning.
- Provide quick predictions through a web application.
- Display confidence scores and important keywords.
- Connect the frontend, backend, and ML model.
- Develop a user-friendly system for analyzing news content.

## 5. System Architecture

The system follows this workflow:

User Input → Flask Backend → Text Preprocessing → TF-IDF Vectorization → Naive Bayes Model → Prediction, Confidence Score, and Keywords

## 6. Machine Learning Pipeline

### 6.1 Data Collection

The system uses a labeled Fake and Real News Dataset from Kaggle.

- Fake news is labeled as 0.
- Real news is labeled as 1.

### 6.2 Data Preprocessing

The news text is cleaned before training the model.

The preprocessing steps include:
- Converting text to lowercase.
- Removing punctuation and special characters.
- Removing common stopwords using NLTK.
- Handling missing and empty values.

### 6.3 Feature Engineering

TF-IDF (Term Frequency–Inverse Document Frequency) converts text into numerical features that the Machine Learning model can process.

It assigns importance to words and phrases in the news content. The system uses unigrams and bigrams to consider individual words and two-word combinations.

### 6.4 Model Selection

The project uses the Multinomial Naive Bayes algorithm.

It is suitable for text classification because it is fast, efficient, and works well with text-based features.

### 6.5 Model Evaluation

The dataset is divided into training and testing sets using an 80:20 split.

The model is evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

The expected accuracy is approximately 90–95%, depending on the dataset and evaluation results. The actual accuracy should be reported after testing the trained model.

## 7. Explainability Feature

The system displays important keywords from the submitted news text to help users understand the prediction.

**Example:**

Input: Breaking shocking news revealed

Output: Important keywords include breaking, shocking, and revealed.

These keywords help explain the text being analyzed but do not independently prove whether the news is true or false.

## 8. Prediction System

**Input:** A news headline or article.

**Output:**
- Prediction: REAL or FAKE
- Confidence score in percentage
- Important keywords

## 9. Backend (Flask API)

The Flask backend provides an API endpoint for making predictions.

The API accepts news text from the frontend, processes the input, and sends back the prediction, confidence score, and important keywords.

**Backend Features**
- REST API development using Flask.
- Loading trained Machine Learning models.
- Real-time text prediction.
- Communication between frontend and backend.
- Input validation and error handling.

## 10. Frontend and User Interaction

The frontend provides an interface where users can enter a news headline or article and view the prediction results.

**Main Features**
- Text input area for news content.
- Button to analyze the news.
- Result display showing REAL or FAKE.
- Confidence score.
- Important keywords.

The frontend is developed using HTML, CSS, and JavaScript.

## 11. Project Structure

The project contains the following main files and folders:

- **index.html:** Main user interface.
- **script.js:** Frontend interactions.
- **style.css:** Page styling.
- **models:** Stores the trained Machine Learning model and TF-IDF vectorizer.
- **notebooks:** Contains data analysis notebooks.
- **src:** Contains preprocessing, training, prediction, and utility files.
- **templates:** Contains HTML templates.
- **application.py:** Flask application.
- **config.py:** Application configuration.
- **requirements.txt:** Project dependencies.
- **Procfile:** Deployment configuration.
- **README.md:** Project documentation.

## 12. How to Run the Project Locally

1. Download or clone the project repository.
2. Install the required Python dependencies.
3. Run the text preprocessing process.
4. Train the Machine Learning model.
5. Test the prediction system.
6. Start the Flask server.
7. Open the frontend in a browser and enter news content to view the results.

## 13. Future Improvements

- Integrate advanced NLP models such as BERT.
- Add fact-checking API integration.
- Support multiple languages.
- Improve contextual analysis.
- Deploy the application on cloud platforms such as AWS or Render.

## 14. Conclusion

VerifyAI demonstrates how Machine Learning and NLP can be used to classify news content as real or fake. The project combines a web interface, a Flask backend, and a trained Machine Learning model to provide quick predictions and confidence scores.

The system can help users assess news content, but its predictions should not be treated as definitive proof of authenticity.