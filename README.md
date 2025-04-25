
# Ticket Booking System

## Overview

The Ticket Booking System is a Django-based web application that allows users to view available shows, book tickets, and view their booking history. Users can register, log in, and manage their bookings. The system keeps track of available seats for each show and prevents users from booking more tickets than available.

## Features

- **User Registration**: Users can register for an account to access booking features.
- **User Login/Logout**: Secure login and logout functionality.
- **View Shows**: Displays a list of available shows with dates and times.
- **Book Tickets**: Users can book tickets for a show, specifying the number of seats.
- **Booking History**: Users can view their past bookings and the number of seats booked.
- **Seat Availability**: Available seats for each show are displayed, and users can only book as many seats as are available.

## Tech Stack

- **Backend**: Django (Python)
- **Frontend**: HTML, CSS (with a custom theme)
- **Database**: SQLite (default for Django, can be configured for others)

## Installation

Follow these steps to set up the project locally.

### Prerequisites

- Python 3.8+ installed on your machine.
- pip for managing Python packages.

### Steps

1. **Clone the repository**

    ```bash
    git clone https://github.com/yourusername/ticket-booking-system.git
    cd ticket-booking-system
    ```

2. **Create a virtual environment**

    ```bash
    python -m venv venv
    ```

3. **Activate the virtual environment**

    - On Windows:
      ```bash
      venv\Scripts\activate
      ```

    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

4. **Install dependencies**

    ```bash
    pip install -r requirements.txt
    ```

5. **Migrate the database**

    ```bash
    python manage.py migrate
    ```

6. **Create a superuser (optional, for admin access)**

    ```bash
    python manage.py createsuperuser
    ```

7. **Run the development server**

    ```bash
    python manage.py runserver
    ```

8. **Open the application in your browser**

    Go to `http://127.0.0.1:8000/` to access the site.
   
9. **Screenshots**
  ![Screenshot 2025-04-25 190038](https://github.com/user-attachments/assets/5f471d02-570e-4ed0-b64a-056476d3e6b4)
#![Screenshot 2025-04-25 190119](https://github.com/user-attachments/assets/24b08847-2bf7-480a-bdb4-cdb8af69e9ec)
![Screenshot 2025-04-25 190106](https://github.com/user-attachments/assets/5e23d45e-1d25-4710-8152-30af10447ef0)
![Screenshot 2025-04-25 190052](https://github.com/user-attachments/assets/e9665e25-a44c-46c0-bd67-d41267e855cc)
# Directory Structure

```
ticket-booking-system/
├── booking/                   # Main app directory
│   ├── migrations/             # Database migrations
│   ├── templates/              # HTML templates
│   │   ├── user/               # User-related templates (home, booking, etc.)
│   │   └── admin/              # Admin-related templates
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py                # Views handling the logic
│   └── urls.py                 # URL routing
├── manage.py                  # Django's command-line utility
├── db.sqlite3                 # SQLite database (default)
├── requirements.txt           # Project dependencies
└── README.md                  # This file
```

## Usage

1. **Register a User**: Navigate to the registration page and create an account to get started.
2. **Login**: After registering, log in to access ticket booking features.
3. **Book Tickets**: Go to the "Home" page, view available shows, and book tickets by specifying the number of seats.
4. **View Booking History**: After booking tickets, you can view your booking history.
