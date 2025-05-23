
# Nerv-DFVD  
AI-powered web application for detecting deepfake videos with high accuracy.

## Overview  
Nerv-DFVD was developed as a collaborative group project focused on building a secure and scalable system for identifying manipulated video content. The platform leverages deep learning techniques to analyze video files for signs of facial forgery, providing an accessible tool for digital media integrity.

## Features  
- User authentication and session management 
- Video upload and asynchronous processing 
- Deepfake detection via a pre-trained ML model 
- User dashboard with detection history and results

## Installation  

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd Nerv-DFVD
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Apply database migrations:
   ```bash
   python manage.py migrate
   ```

5. Create a superuser for admin access:
   ```bash
   python manage.py createsuperuser
   ```

6. Run the development server:
   ```bash
   python manage.py runserver
   ```

7. Access the app at:
   ```bash
   http://127.0.0.1:8000
   ```

## Usage  

1. Register or log in using your credentials. 
2. Upload a video file for analysis. 
3. Wait for the system to complete detection. 
4. Access and review results through your user profile.

## Technology Stack  

- **Backend:** Django 
- **ML Framework:** TensorFlow 
- **Computer Vision:** OpenCV 
- **Database:** SQLite (development) — configurable for production environments

## Contributing  

This project was developed collaboratively and welcomes further contributions. Feel free to fork the repository and submit pull requests for improvements or new features.

## License  

Licensed under the Apache License 2.0. See the `LICENSE` file for details.

## File Structure

```bash

C:.
│   LICENSE
│   manage.py
│   README.md
│   
├───app
│   │   admin.py
│   │   apps.py
│   │   forms.py
│   │   models.py
│   │   tests.py
│   │   urls.py
│   │   views.py
│   │   __init__.py
│   │
│   └───migrations
│           __init__.py
│
├───detection_unit
│       asgi.py
│       settings.py
│       urls.py
│       wsgi.py
│       __init__.py
│
├───models
│       Ken.h5
│
├───notebooks
│       final.ipynb
│       usinglstmcnn.ipynb
│
└───templates
        base.html
        landing_page.html
        results.html
        upload.html
