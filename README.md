# SurveyLens

SurveyLens is a comprehensive survey management and analysis application powered by Django and AI technologies. It revolutionizes the survey experience by using AI chatbots for both conducting surveys and providing analytical insights to administrators.

## Features

### 🌟 Public User Features
*   **Interactive Dashboard**: Personalized dashboard for users.
*   **AI Survey Chatbot**: engaging, conversational survey experience instead of static forms.
*   **Secure Authentication**: User signup, login, and secure session management.

### 🛡️ Administrator Features
*   **Admin Dashboard**: Real-time statistics and overview of survey performance.
*   **AI Insight Assistant**: dedicated chatbot for admins to query survey data and get insights.
*   **Survey Management**: View survey history and detailed responses.
*   **Automated Reporting**: Generate professional PDF reports for survey results.

## Technology Stack

*   **Backend Framework**: Django 5.2
*   **API**: Django REST Framework
*   **Database**: PostgreSQL
*   **AI & ML**:  OpenAI (for chatbot functionalities)
*   **Dependencies**: `aiohttp`,  `openai`, `reportlab` (implied for PDF), etc.

## Installation & Setup

### Prerequisites
*   Python 3.10+
*   PostgreSQL

### 1. Clone the project
```bash
git clone <repository-url>
cd ideahive
```

### 2. Create and activate a visual environment
```bash
python -m venv env
# Windows
.\env\Scripts\activate
# Linux/Mac
source env/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configuration
Create a `.env` file in the project root (`f:\ideahive`) and add your API keys:

```env
USER_API=your_google_genai_or_openai_key_here
ADMIN_API=your_admin_bot_api_key_here
```
> **Note**: Update `surveylens/settings.py` database configuration if your PostgreSQL credentials differ from the defaults.

### 5. Database Setup
Ensure PostgreSQL is running and create the database:
```sql
CREATE DATABASE surveylens;
```

Apply migrations:
```bash
cd surveylens
python manage.py makemigrations
python manage.py migrate
```

### 6. Run the Server
```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` to access the application.

## Project Structure

*   `autho/`: Authentication and landing page logic.
*   `administator/`: Admin dashboard, analytics, and reporting tools.
*   `public_user_app/`: User dashboard and survey-taking interface.
*   `surveylens/`: Core project settings and configurations.
