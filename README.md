
# Remote Job Market Data Pipeline

## Description
This project implements an end-to-end data pipeline to extract, clean, and load remote job postings from a REST API into a PostgreSQL database. The pipeline automates the ingestion and preparation of job market data, facilitating in-depth analysis and reporting to derive actionable insights on remote employment trends.

## Features
*   **Data Extraction:** Fetches remote job postings from a third-party REST API.
*   **Data Cleaning & Transformation:** Utilizes pandas for data manipulation, including handling missing values, standardizing formats, and extracting relevant information from raw data.
*   **Database Loading:** Loads the cleaned and transformed data into a PostgreSQL database.
*   **Environment Management:** Uses `python-dotenv` for secure management of API keys and database credentials.

## Technologies Used
*   **Python:** Primary programming language.
*   **Pandas:** For data manipulation and analysis.
*   **Requests:** For making HTTP requests to the REST API.
*   **Psycopg2:** PostgreSQL adapter for Python.
*   **SQLAlchemy:** ORM for database interaction.
*   **BeautifulSoup:** For parsing HTML content (e.g., job descriptions).
*   **python-dotenv:** For managing environment variables.
*   **PostgreSQL:** Relational database for storing job data.
*   **Jupyter Notebook:** For iterative development and data exploration (`src/pipeline.ipynb`).

## Setup Instructions

### Prerequisites
*   Python 3.8+
*   PostgreSQL installed and running
*   A RapidAPI key for the "Remote Jobs" API

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Ohenedarkoh/Remote-jobs-api-to-postgre.git
    cd Remote-jobs-api-to-postgre
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate # On Windows
    source venv/bin/activate # On macOS/Linux
    ```

3.  **Install the required Python packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up environment variables:**
    Create a `.env` file in the project root directory with the following variables:
    ```
    API_KEY="YOUR_RAPIDAPI_KEY"
    API_HOST="remote-jobs1.p.rapidapi.com"
    POSTGRESQL_DB="your_database_name"
    POSTGRESQL_USER="your_username"
    POSTGRESQL_PASSWORD="your_password"
    POSTGRESQL_HOST="localhost"
    POSTGRESQL_PORT="5432"
    ```
    Replace the placeholder values with your actual RapidAPI key and PostgreSQL database credentials.

## Usage

1.  **Run the data pipeline:**
    Open the Jupyter Notebook `src/pipeline.ipynb` and execute all cells sequentially. This will:
    *   Fetch job data from the API.
    *   Clean and transform the data.
    *   Load the final dataset into your PostgreSQL database.

2.  **Verify data in PostgreSQL:**
    Connect to your PostgreSQL database using your preferred tool and query the `remote_jobs` table to verify the loaded data.



## Contact

[Frank Ohene-Darkoh] - [ohenedarkohfrank@gmail.com] - [[Your LinkedIn Profile URL](https://www.linkedin.com/in/frankohene-darkoh-44412222b)]