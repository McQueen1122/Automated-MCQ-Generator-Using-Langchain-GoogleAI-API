# MCQ Generator

## Project Description
MCQ Generator is an innovative tool that automatically generates multiple-choice questions (MCQs) from a given text file. This project harnesses the power of Langchain and OpenAI's API to create relevant and challenging questions based on the content provided.

## Features
- Reads content from a text file
- Generates multiple-choice questions based on the content
- Utilizes Langchain and OpenAI's API for natural language processing
- Customizable inputs for question generation
- Provides both quiz questions and a review

## Installation

### Prerequisites
- Python 3.7+ and below 3.10

### Setup
1. Clone the repository:
    git clone https://github.com/McQueen1122/mcq_gen cd mcq-generator
2. Install the required packages:
    pip install -r requirements.txt
3. Set up your environment variables:
    Create a `.env` file in the root directory and add your OpenAI API key:
    OPENAI_API_KEY=your_api_key_here
    streamlit run app.py


## How it Works
The MCQ Generator uses a Langchain Sequential Chain with two main components:
1. `quiz_chain`: Generates the MCQ questions
2. `review_chain`: Provides a review of the generated questions

The chain is defined as follows:
```python
generate_evaluate_chain = SequentialChain(
    chains=[quiz_chain, review_chain],
    input_variables=["text", "number", "subject", "tone", "response_json"],
    output_variables=["quiz", "review"],
    verbose=True
)
```
## Inputs:

- **Inputs**:
    - `text`: The content from which to generate questions
    - `number`: The number of questions to generate
    - `subject`: The subject area of the content
    - `tone`: The desired tone of the questions
    - `response_json`: JSON format for the response (internal use)

- **Outputs**:
    - `quiz`: The generated MCQ questions
    - `review`: A review of the generated questions

- **Dependencies**:
    - `openai`
    - `langchain`
    - `streamlit`
    - `python-dotenv`
    - `PyPDF2`

## Contributing
Contributions to improve MCQ Generator are welcome. Please feel free to submit a Pull Request.

## version
0.0.0   

## Contact
McQueen - mcqueen1121@outlook.com

https://github.com/McQueen1122/mcq_gen