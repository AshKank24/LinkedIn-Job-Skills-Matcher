# LinkedIn Job Skills Matcher

This project automates the process of extracting and matching skills between job descriptions and candidate profiles on LinkedIn using web scraping, natural language processing, and machine learning techniques.

## Features

- Automates login and navigation on LinkedIn
- Extracts job descriptions and candidate skills using Selenium and BeautifulSoup
- Preprocesses and extracts keywords from text using NLTK
- Computes similarity scores between job skills and candidate skills using Sentence Transformers (BERT)
- Outputs an overall similarity score for candidates

## Requirements

- Python 3.6+
- Selenium
- BeautifulSoup
- NLTK
- Sentence Transformers
- Scikit-learn

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/linkedin-job-skills-matcher.git
    cd linkedin-job-skills-matcher
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Download necessary NLTK data:

    ```python
    import nltk
    nltk.download('stopwords')
    nltk.download('punkt')
    nltk.download('averaged_perceptron_tagger')
    ```

## Usage

1. Update the `username` and `password` variables in the script with your LinkedIn credentials.
2. Ensure you have the appropriate WebDriver (e.g., `chromedriver`) installed and in your PATH.
3. Run the script:

    ```bash
    python linkedin_job_skills_matcher.py
    ```

## Script Overview

1. **Login to LinkedIn:**

    The script logs in to LinkedIn using the provided credentials.

    ```python
    username = "your_email@example.com"
    password = "your_password"
    ```

2. **Navigate to Job Posting Page:**

    The script navigates to the job posting page and extracts the job description.

    ```python
    driver.get(job_link)
    ```

3. **Extract and Preprocess Skills:**

    Extract skills from job descriptions and candidate profiles, and preprocess the text.

    ```python
    def extract_skills(job_description):
        # Extract skills from job description
    ```

4. **Compute Similarity Scores:**

    Compute similarity scores between job skills and candidate skills using BERT embeddings.

    ```python
    model = SentenceTransformer('all-MiniLM-L6-v2')
    ```

5. **Output Results:**

    Output the overall similarity score for the candidate.

    ```python
    print(f"Overall similarity score for the candidate: {overall_score:.2f}")
    ```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
