
# MCQ Generator Application

This project is a web application designed to generate Multiple Choice Questions (MCQs) based on text extracted from uploaded PDF or TXT files. It uses Flask as the web framework and incorporates Natural Language Processing (NLP) techniques for text analysis and question generation.

## Features

- **Multiple File Upload**: Users can upload multiple PDF or TXT files containing the text from which MCQs will be generated.
- **MCQ Generation**: The application generates a specified number of MCQs based on the uploaded text using NLP techniques.
- **Interactive UI**: A user-friendly interface built with Bootstrap for a modern look and feel.
- **Results Display**: Users can reveal the correct answers after attempting the MCQs.

## Installation

### Prerequisites

- Python 3.6 or higher
- pip (Python package installer)

### Steps

1. **Clone the repository**:

    ```bash
    git clone https://github.com/your-username/mcq-generator.git
    cd mcq-generator
    ```

2. **Create a virtual environment**:

    ```bash
    python -m venv venv
    ```

3. **Activate the virtual environment**:

    - On Windows:
        ```bash
        venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

4. **Install the required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Flask application**:

    ```bash
    python app.py
    ```

2. **Open your web browser and navigate to**:

    ```
    http://127.0.0.1:5000/
    ```

3. **Upload your files**:
   - Click on the file upload button and select your PDF or TXT files.
   - Specify the number of MCQs you want to generate.
   - Click "Generate MCQs".

4. **Review the MCQs**:
   - The generated MCQs will be displayed on a new page.
   - Answer the MCQs and click "Show Results" to see the correct answers.

## Project Structure

```
.
├── app.py
├── requirements.txt
├── templates
│   ├── index.html
    └── mcqs.html
```

- `app.py`: Main application file containing the Flask routes and logic.
- `requirements.txt`: Lists all the dependencies required for the project.
- `templates/`: Contains the HTML templates for the web pages.

## Technical Details

### Flask

- **Flask** is a lightweight WSGI web application framework in Python. It is designed to make getting started quick and easy, with the ability to scale up to complex applications.

### File Upload

- **File Handling**: The application handles file uploads using Flask's `request.files` object.
- **Secure Filename**: Uploaded files are saved with secure filenames using `werkzeug.utils.secure_filename`.

### Text Extraction

- **PDF Extraction**: Text is extracted from PDF files using the `PyPDF2` library.
- **TXT Handling**: Text files are read directly and their contents are used for MCQ generation.

### MCQ Generation

- **Natural Language Processing (NLP)**: The application uses NLP techniques to analyze the text and generate relevant MCQs. This involves tokenizing the text, identifying key concepts, and formulating questions and multiple-choice answers.
- **Dummy Function**: A placeholder function simulates MCQ generation by creating sample questions and choices. This can be replaced with a more sophisticated NLP-based algorithm for real applications.

### Frontend

- **Bootstrap**: The application uses Bootstrap 4.5.2 for responsive design and modern UI elements.
- **JavaScript**: A small JavaScript snippet is included to handle the display of correct answers.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
