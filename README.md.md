
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

## Directory Structure

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

## Troubleshooting

- **Error: "Not enough available seats"**: Ensure that you're not trying to book more seats than are available for the selected show.
- **Error: "Cannot assign AnonymousUser"**: Ensure that you are logged in before attempting to book tickets.

## Contributing

1. Fork the repository.
2. Create a new branch for your feature.
3. Commit your changes.
4. Push to your fork.
5. Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
