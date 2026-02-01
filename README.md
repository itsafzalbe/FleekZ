# FleekZ

FleekZ is a web-based video sharing platform project that allows users to upload, view, and interact with videos in a modern, streamlined interface.

The project demonstrates core backend and frontend concepts such as authentication, media handling, user interactions, and third-party cloud integration.

---

## Features

- User registration and authentication
- Video upload and deletion
- Video streaming and optimization
- Automatic thumbnail generation
- Custom thumbnail support
- Like and dislike system
- View count tracking
- User channels
- Watermarked thumbnails
- Responsive layout with fixed navbar and collapsible sidebar

---

## Tech Stack

### Backend
- Python
- Django
- Django Authentication System

### Frontend
- HTML
- CSS
- JavaScript (vanilla)

### Media & Storage
- ImageKit (video hosting, streaming, thumbnails, optimization)

### Database
- SQLite (default, configurable)

---

## Project Structure (Simplified)
```bash
fleekz/
├── account/          # User registration and authentication
├── videos/           # Video models, views, and logic
├── static/           # CSS, JS, and assets
├── templates/        # HTML templates
├── manage.py
└── requirements.txt
```

---

## Authentication

- User registration using a custom signup form
- Automatic login after successful registration
- Login required for:
  - Uploading videos
  - Liking / disliking videos
  - Deleting videos

---

## Video System

- Videos are uploaded and stored via **ImageKit**
- Multiple video URLs are generated:
  - Optimized video URL
  - Streaming (HLS) URL
  - Thumbnail URL
- Thumbnails can be:
  - Auto-generated
  - Custom uploaded
- Thumbnails are dynamically watermarked with the uploader’s username

---

## Likes & Dislikes

- Users can like or dislike a video
- Only one reaction per user per video
- Clicking the same reaction again removes it
- Like and dislike counts update dynamically

---

## Channels

- Each user has a channel page
- Channel pages display all videos uploaded by the user

---

## Installation & Setup
```bash
1️. Clone the repository

git clone <your-repo-url>
cd fleekz

2️. Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

3️. Install dependencies
pip install -r requirements.txt

4️. Environment variables
Create a .env file and add your ImageKit credentials:
IMAGEKIT_PUBLIC_KEY=your_public_key
IMAGEKIT_PRIVATE_KEY=your_private_key
IMAGEKIT_URL_ENDPOINT=your_url_endpoint

5️. Run migrations
python manage.py migrate

6️. Create superuser (optional)
python manage.py createsuperuser

7️. Run the server
python manage.py runserver

Open:
http://127.0.0.1:8000/
```

# Project Purpose

This project was developed as a learning and demonstration project to showcase:
	•	Django backend development
	•	Media handling with third-party services
	•	User authentication workflows
	•	Clean project structure
	•	Interactive frontend behavior



# License

This project is intended for educational purposes.
