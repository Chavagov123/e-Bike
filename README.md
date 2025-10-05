# eBike Management App

This is a simple CRUD (Create, Read, Update, Delete) application built with Streamlit to manage eBike dealer information. It uses a MySQL database to store the data.

## Features

- **Add:** Add new dealer information, including ID, name, city, PIN code, and street.
- **View:** View all dealer information in a table and see a pie chart visualizing dealer locations by city.
- **Edit:** Update the details of existing dealers.
- **Remove:** Delete dealers from the database.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.6+
- MySQL Server

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/eBike_with_streamlit.git
    cd eBike_with_streamlit
    ```

2.  **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

## Database Setup

1.  **Start your MySQL server.**

2.  **Create the database:**
    Log in to your MySQL client and run the following command to create the necessary database:
    ```sql
    CREATE DATABASE e_bike;
    ```

3.  **Configure the database connection:**
    Open the `eBike_with_streamlit/database.py` file and update the database connection details with your MySQL credentials:

    ```python
    mydb = mysql.connector.connect(
        host="localhost",
        user="your_mysql_username",  # Update with your username
        password="your_mysql_password",  # Update with your password
        database="e_bike"
    )
    ```
    The application will automatically create the `DEALER` table when it first runs.

## How to Run the Project

1.  **Navigate to the project directory:**

    ```bash
    cd path/to/your/project/folder
    ```

2.  **Run the Streamlit application:**

    ```bash
    streamlit run eBike_with_streamlit/app.py
    ```

    The application will open in your default web browser. You can now use the sidebar menu to navigate between the "Add", "View", "Edit", and "Remove" functionalities.