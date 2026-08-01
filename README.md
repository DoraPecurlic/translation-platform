# Translation Platform
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-4.1.6-092E20?logo=django&logoColor=white)
![Database](https://img.shields.io/badge/Database-SQLite-003B57?logo=sqlite&logoColor=white)
![Frontend](https://img.shields.io/badge/Frontend-Bootstrap%205-7952B3?logo=bootstrap&logoColor=white)

A Django-based marketplace prototype that connects clients who need text translations with translators looking for work.

Clients can publish translation jobs, define the language pair, provide the source text and set a budget.
Translators can browse available jobs and submit bids, while clients can select a translator and follow the job through delivery. The application also includes user profiles, token balances, ratings, disputes and direct messaging.

## Features

- User registration, authentication and profile management
- Separate client and translator workflows
- Translation jobs with source and target languages, domain, budget and text
- Job browsing and bid submission for translators
- Bid acceptance and translation delivery workflow
- Token-based payments between clients and translators
- Translator ratings and dispute reporting
- Direct messaging between users
- Personal dashboards for jobs, bids and account activity

## Application Workflow

1. A client creates a translation job.
2. Translators browse the available jobs and submit bids.
3. The client accepts a bid and assigns the job.
4. The selected translator submits the completed translation.
5. The client rates the work, and the agreed number of tokens is transferred to the translator.

## Technology Stack

| Area | Technology |
| --- | --- |
| Backend | Python, Django 4.1.6 |
| Frontend | Django Templates, Bootstrap 5, CSS |
| Database | SQLite |
| Forms | Django Forms, django-widget-tweaks |
| Authentication | Django authentication system |

## Project Structure

```text
Translate-App/
└── translateapp/
    ├── accounts/       # Registration, profiles and dashboards
    ├── app/            # Jobs, bids, ratings and disputes
    ├── messenger/      # Direct user messaging
    ├── translateapp/   # Django project configuration
    ├── manage.py
    └── requirements.txt
```

## Running the Project

1. Clone the repository and open the application directory:

   ```bash
   git clone https://github.com/DoraPecurlic/Translate-App.git
   cd Translate-App/translateapp
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   ```

   On Windows PowerShell:

   ```bash
   .\.venv\Scripts\Activate.ps1
   ```

3. Install the dependencies and prepare the database:

   ```bash
   python -m pip install -r requirements.txt
   python manage.py migrate
   ```

4. Start the development server:

   ```bash
   python manage.py runserver
   ```

5. Open `http://127.0.0.1:8000/` in a browser.
