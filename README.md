Vehicle Information Portal - Web Scraping with Django
This project is a Vehicle Information Portal that allows users to view detailed information about motorcycles. The application is built using Django as the web framework, and BeautifulSoup for web scraping to fetch real-time data about motorcycles. The data is stored in an SQLite database.

Features
Web Scraping: Real-time data fetched from an external website (using BeautifulSoup).
Django-based web application: User-friendly interface to display motorcycle information.
SQLite Database: Stores motorcycle specifications and scraped data.
Responsive UI: A responsive and mobile-friendly design for easy navigation.
Technologies Used
Python 3.x
Django: Web framework for building the portal.
BeautifulSoup: Library for web scraping to extract real-time data.
SQLite: Lightweight database for storing vehicle information.
HTML/CSS: For creating the front-end of the application.
Bootstrap: Framework for styling the UI components.
Git: Version control for the project.
Installation and Setup
Follow these steps to set up the project on your local machine:

Prerequisites
Make sure you have Python and pip installed on your machine. You can check by running:

bash
Copy
python --version
pip --version
1. Clone the Repository
Clone the project repository to your local machine:

bash
Copy
git clone https://github.com/allemkarthik/Bike-Django-project.git
cd Bike-Django-project
2. Install Dependencies
Create a virtual environment and activate it:

bash
Copy
python -m venv venv
source venv/bin/activate  # For Mac/Linux
venv\Scripts\activate     # For Windows
Install the required dependencies:

bash
Copy
pip install -r requirements.txt
If the requirements.txt file is not available, you can install the necessary libraries manually:

bash
Copy
pip install django beautifulsoup4 requests sqlite3
3. Run Database Migrations
Run the following command to set up the SQLite database:

bash
Copy
python manage.py migrate
4. Run the Development Server
Now, you can run the Django development server to start the application:

bash
Copy
python manage.py runserver
5. Access the Application
Open your web browser and go to http://127.0.0.1:8000/ to see the application in action.

How It Works
Web Scraping:

The BeautifulSoup library is used to scrape real-time data (e.g., specifications of motorcycles) from a predefined external website.
This data is then processed and stored in the SQLite database.
Database:

All motorcycle details (such as model name, engine specifications, price, etc.) are stored in an SQLite database.
The portal fetches data from the database and displays it in a clean, organized format.
User Interface:

The portal has a simple, clean interface where users can browse through various motorcycle details.
It is designed to be responsive and user-friendly across devices.
Usage
Navigate through different sections of the website to view the detailed specifications of various motorcycles.
Refresh the data by running the web scraping process to pull in updated motorcycle data.
Project Structure
Here’s a breakdown of the important files and directories in the project:

graphql
Copy
Vehicle-Information-Portal/
│
├── manage.py                  # Django management script to run server, migrations, etc.
├── vehicle_info/              # Django app that contains the main business logic
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py              # Defines the SQLite database models
│   ├── scraping.py            # Python file for scraping motorcycle data
│   ├── views.py               # Views that render the data in HTML
│   └── templates/
│       └── vehicle_info/
│           └── index.html     # The main page of the vehicle portal
│
├── db.sqlite3                 # SQLite database where motorcycle data is stored
└── requirements.txt           # Python dependencies for the project
Contributing
Contributions are welcome! If you have any suggestions or improvements, feel free to open a pull request or an issue.

Fork the repository.
Create a new branch (git checkout -b feature-name).
Make your changes.
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-name).
Open a pull request.
License
This project is licensed under the MIT License - see the LICENSE file for details.

