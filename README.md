
# Tech Tweet Django Project

This project is a Django-based web application where users can perform CRUD (Create, Read, Update, Delete) operations on "Tech Tweets". The application is designed with user authorization, ensuring that each user can only manage their own tweets. Users cannot edit or delete tweets posted by others.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [API Endpoints](#api-endpoints)
- [Authorization](#authorization)
- [Technologies](#technologies)

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/RutujaGurav07/tech_tweet.git
   cd tech-tweet
   ```

2. **Install dependencies**:
   Make sure you have Python and Django installed. You may want to use a virtual environment.
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. **Run migrations**:
   ```bash
   python manage.py migrate
   ```

4. **Create a superuser**:
   ```bash
   python manage.py createsuperuser
   ```

5. **Start the development server**:
   ```bash
   python manage.py runserver
   ```

## Usage

Once the server is running, you can access the application by navigating to `http://127.0.0.1:8000` in your web browser. Register a new user or log in as the superuser to manage tweets.

## Features

- **User Authentication**: Sign up, log in, and log out functionality.
- **CRUD Operations on Tech Tweets**:
  - **Create**: Users can create new tweets.
  - **Read**: All users can view public tweets.
  - **Update/Delete**: Users can only update or delete their own tweets.
- **Authorization**: Users cannot edit or delete tweets posted by others.

## API Endpoints

- **GET /tweets/**: Retrieve all tweets.
- **POST /tweets/**: Create a new tweet (authentication required).
- **PUT /tweets/<id>/**: Update a specific tweet (only the author can update).
- **DELETE /tweets/<id>/**: Delete a specific tweet (only the author can delete).

## Authorization

Each user is restricted to managing only their own tweets. Attempts to edit or delete another user's tweet will result in an authorization error.

## Technologies

- **Backend**: Django
- **Database**: SQLite (default, replaceable with other databases)
- **Authentication**: Django's built-in user authentication

---

