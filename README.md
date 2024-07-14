# SMS Spam Detector

This project involves creating an SMS text classification solution using a linear Support Vector Classification (SVC) model. The model is then deployed using a Gradio app to enable users to classify text messages as spam or not.

## Project Overview

The main components of this project are:
1. **SMS Classification Function**: Refactoring the provided solution to construct a linear SVC model.
2. **SMS Prediction Function**: Creating a function to predict if a new text message is spam or not.
3. **Gradio Interface Application**: Building a Gradio app to allow users to interact with the model.

## Files in the Repository

- `gradio_sms_text_classification.ipynb`: Jupyter notebook containing the refactored code for SMS classification and the Gradio app.
- `SMSSpamCollection.csv`: Dataset used for training and testing the model.
- `README.md`: Documentation of the project.

## Requirements

### SMS Classification Function

1. **Set Features and Target Variables**:
    - `features`: Text message column of the DataFrame.
    - `target`: "label" column of the DataFrame.

2. **Data Splitting**:
    - Split the data into training and testing sets with a test size of 33%.

3. **Model Pipeline**:
    - Build a pipeline using `TfidfVectorizer` and `LinearSVC`.

4. **Model Training**:
    - Fit the model to the transformed training data and return the model.

### SMS Prediction Function

1. **Prediction**:
    - Predict the classification of a new text message.
    
2. **Conditional Output**:
    - Return a message indicating whether the text is "ham" or "spam".

### Gradio Interface Application

1. **Interface Setup**:
    - Create a Gradio Interface with input and output textboxes.
    
2. **Application Launch**:
    - Provide a public URL to share the application.

## Usage

### Running the Notebook

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Navigate to the project directory and open the Jupyter notebook:
    ```bash
    cd sms_spam_detector
    jupyter notebook gradio_sms_text_classification.ipynb
    ```
3. Follow the instructions in the notebook to run the cells.

### Testing the Application

1. Launch the Gradio app by running the notebook cells related to the Gradio interface.
2. Test the application using the following example text messages:
    - "You are a lucky winner of $5000!"
    - "You won 2 free tickets to the Super Bowl."
    - "You won 2 free tickets to the Super Bowl. Text us to claim your prize."
    - "Thanks for registering. Text 4343 to receive free updates on medicare."

## References

Based on starter files and data provided as part of OSU-VIRT-AI-PT-02-2024-U-LOLC-MTTH (OSU AI Bootcamp) for Challenge 21. Remaining code based on code examples provided as part of the course.

- Tiago, A., & Hidalgo, J. (2012). SMS Spam Collection. UCI Machine Learning Repository. Available at: [https://archive.ics.uci.edu/dataset/228/sms+spam+collection](https://archive.ics.uci.edu/dataset/228/sms+spam+collection)

