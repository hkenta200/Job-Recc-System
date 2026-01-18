# Resume-Based Job-Recc-System

Created using Python (SKLearn, PDFPY2)

Job Reccomendation System that takes in user resumes and compares them to job descriptions (scraped data from glassdoor) using cosine similarity and TFIDF based on vectorized tokens
The output is a list of the _ top jobs. 

This project is an NLP-driven job recommender system that matches a candidate’s resume to the most relevant job postings using **TF-IDF vectorization, cosine similarity, and K-Nearest Neighbors (KNN)**.

The system parses a resume from a PDF file, preprocesses the text, and compares it against a dataset of job descriptions to return ranked job recommendations based on similarity scores.

## 🚀 Key Features

* PDF resume parsing using **PyPDF2**
* Text preprocessing with **NLTK** (tokenization, stopword removal, lemmatization)
* Job description vectorization using **TF-IDF**
* Similarity matching using **Cosine Similarity**
* Nearest-neighbor ranking using **KNN (scikit-learn)**
* Returns top-N job recommendations with similarity scores

## 🧠 How It Works

1. **Load Data**

   * Resume is extracted from a PDF file
   * Job descriptions are loaded from a CSV dataset

2. **Text Preprocessing**

   * Lowercasing
   * Stopword and punctuation removal
   * Tokenization
   * Lemmatization

3. **Vectorization**

   * Job descriptions are transformed into TF-IDF vectors
   * Resume text is transformed using the same TF-IDF model

4. **Similarity Matching**

   * Cosine similarity measures relevance between resume and each job description
   * KNN identifies the closest job descriptions in vector space

5. **Ranking & Output**

   * Jobs are ranked by similarity score
   * Top job recommendations are returned in a DataFrame

## 🧰 Tech Stack

* **Python 3.8+**
* **scikit-learn**
* **NLTK**
* **PyPDF2**
* **Pandas / NumPy**

## 📂 Project Structure

```text
.
├── (FINAL)_626IRProject(Job_Reccomendation_System).ipynb           # Main notebook / script
├── RandomResume.pdf                                                # Sample resume (PDF)
├── RandomResume2.pdf                                               # Main notebook / script
├── requirements.txt                                                # Python dependencies
├── jobs_data.csv                                                   # jobs data set 
└── README.md
```

## 📊 Dataset

This project uses a Kaggle job listings dataset:

* **Dataset:** Salary & Job Descriptions Dataset
* **Source:** Kaggle (Glassdoor job postings)

Download the dataset and place the CSV file in the project root directory.

## ▶️ Installation & Setup

1. Clone the repository:

```bash
git clone <your-repo-url>
cd <project-folder>
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Download required NLTK resources:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

## ▶️ Running the Project

1. Place your resume PDF in the project directory
2. Update the resume file path in the code:

```python
reader = PdfReader("YourResume.pdf")
```

3. Adjust the number of job recommendations:

```python
num_jobs = 20
```

4. Run the script or notebook

## 📈 Output Example

The system outputs a ranked table containing:

* Company Name
* Job Title
* Similarity Score
* Job Description
* Salary Estimate

Higher similarity scores indicate better matches between the resume and job description.


## 🙌 Acknowledgements

* scikit-learn
* NLTK
* Kaggle datasets
* Glassdoor job listings
