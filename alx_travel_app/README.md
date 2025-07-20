# ALX Travel App 0x00

A Django RESTful API project for managing travel listings, bookings, and reviews. Integrated with Swagger for documentation, MySQL for the database, Celery for task management, and seeders for demo data.

---

## Features

* Manage travel listings with title, description, location, pricing, and availability.
* Bookings with user linkage and date range.
* Reviews with ratings and comments.
* Seed command to populate sample listings.
* REST API endpoints with Swagger UI.

---

## Technologies Used

* Django 4.2+
* MySQL
* Django REST Framework
* drf-yasg (Swagger)
* Celery
* Redis (for Celery broker)
* django-environ

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/alx_travel_app_0x00.git
cd alx_travel_app_0x00/alx_travel_app
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Setup .env file

Create a `.env` file at the project root:

```env
SECRET_KEY=your-secret-key
DEBUG=True
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=localhost
DB_PORT=3306
```

### 5. Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Seed the database

```bash
python manage.py seed
```

### 7. Run the server

```bash
python manage.py runserver
```

Visit Swagger UI at:

```
http://127.0.0.1:8000/swagger/
```

---

## Project Structure

```
alx_travel_app/
├── alx_travel_app/
│   ├── settings.py
│   ├── urls.py
│   └── celery.py
├── listings/
│   ├── models.py
│   ├── serializers.py
│   ├── urls.py
│   ├── views.py
│   └── management/commands/seed.py
├── templates/
├── static/
└── .env
```

---

## Seed Command Details

The seed command creates 10 sample `Listing` entries.

```bash
python manage.py seed
```

You can expand it to also seed users, bookings, and reviews.

---

## API Endpoints

* `GET /api/listings/` - List all listings
* `POST /api/bookings/` - Create a booking
* More endpoints coming soon

---

