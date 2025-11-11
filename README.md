# Django-Project-2: School Management System for School №30

## Overview

**Django-Project-2** is a full-stack web application built using the Django framework, designed as a comprehensive management system for School №30 in Ussuriysk. This project serves as a practical tool for handling school operations, including staff profiles, news announcements, job vacancies, document storage, sponsor information, and user feedback. It can be used as a portfolio piece, a template for similar educational websites, or deployed for real-world use by schools.

The application emphasizes ease of administration through Django's built-in admin panel, while providing a user-friendly interface for visitors, parents, and staff. It demonstrates advanced Django features like model relationships, filtering, image handling, and form processing. Built with responsiveness in mind, it ensures accessibility on all devices. This project is ideal for developers learning Django, as it includes modular code, comments, and real-world integrations.

If you're new to web development, fork this repo to customize it for your own school or organization. The codebase prioritizes security (e.g., authentication for admin tasks), performance, and scalability, making it suitable for small to medium-sized institutions.

## Key Features

- **Staff Management**: Detailed profiles for teachers and staff, including bios, photos, positions, and contact details. Easily searchable and filterable.

- **News and Announcements System**: Categorized news feed with posts, images, and dates. Supports filtering by categories (e.g., events, updates) using django-filters.

- **Vacancy Board**: Section for posting and viewing current job openings, with descriptions, requirements, and application instructions.

- **Document Repository**: Upload and organize important school documents (e.g., policies, forms) for easy download by users.

- **Sponsor Information**: Pages dedicated to school sponsors, with logos, descriptions, and links to their websites.

- **Feedback and Contact System**: User-friendly contact form for inquiries, suggestions, or complaints, integrated with email notifications.

- **School Sections**: Dedicated pages for:
  - About the School (history, mission, facilities).
  - Contact Information (address, phone, email, map integration if added).
  - Responsive navigation for seamless browsing.

- **Admin Dashboard**: Customized Django admin interface for managing all content, with inline editing, search, and filters.

- **Responsive Design**: Mobile-first layout using HTML/CSS, ensuring the site works well on desktops, tablets, and phones.

- **Additional Enhancements**: Image processing for uploads (via Pillow), basic SEO meta tags, and potential for future expansions like user authentication for parents/students.

## Tech Stack

- **Backend**: Django 5.2 (Python 3.8+)
- **Frontend**: HTML5, CSS3
- **Database**: SQLite (default; configurable for PostgreSQL or MySQL)
- **Other Libraries**:
  - django-filters for news and staff categorization.
  - Pillow for image handling and thumbnails.
- **Deployment Tools**: Gunicorn + Nginx (recommended for production), or platforms like Heroku for quick setup.

## Installation

Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```
   git clone https://github.com/waratecs123/Django-Project-2.git
   cd Django-Project-2
   ```

2. **Create a Virtual Environment**:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```
   pip install -r requirements.txt
   ```

4. **Set Up Environment Variables** (optional for production):
   - Create a `.env` file in the root directory.
   - Add keys like `SECRET_KEY=your_secret_key`, `DEBUG=False`, `EMAIL_HOST_USER=your_email`.

5. **Apply Migrations and Create Superuser**:
   ```
   python manage.py makemigrations
   python manage.py migrate
   python manage.py createsuperuser
   ```

6. **Run the Development Server**:
   ```
   python manage.py runserver
   ```
   Access the site at `http://127.0.0.1:8000/`.

For production deployment, refer to Django's official docs on deploying with Heroku, AWS, or DigitalOcean.

## Usage

- **Admin Access**: Navigate to `/admin/` and log in with your superuser credentials to manage staff, news, vacancies, documents, and more.
- **Customize Content**: Edit models in the respective app's `models.py` files or use fixtures for initial data (e.g., `python manage.py loaddata fixtures/initial_data.json`).
- **Adding Entries**: Use the admin panel to upload images, create news posts, or add staff profiles.
- **Testing**: Run unit tests with `python manage.py test`.
- **Demo**: Deploy to a platform like Heroku and link a live demo here (e.g., [Live Demo](https://your-app.herokuapp.com)).

## Code Structure

```
Django-Project-2/
├── manage.py
├── requirements.txt
├── school_system/         # Main project folder
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── staff/                 # App for staff management
│   ├── migrations/
│   ├── templates/staff/
│   ├── __init__.py
│   ├── admin.py
│   ├── models.py         # Staff models (e.g., Teacher, Position)
│   ├── views.py
│   ├── urls.py
│   └── forms.py
├── news/                  # App for news and announcements
│   ├── ... (similar structure)
├── vacancies/             # App for job vacancies
│   ├── ... 
├── documents/             # App for document repository
│   ├── ... 
├── sponsors/              # App for sponsor information
│   ├── ... 
├── feedback/              # App for contact/feedback forms
│   ├── ... 
├── static/                # CSS, JS, images
├── templates/             # Base HTML templates
├── media/                 # Uploaded files (staff photos, documents)
└── .gitignore
```

- Apps are modular: Each feature (e.g., `staff`, `news`) is in its own app for better organization.
- Templates use inheritance from `base.html` for consistent layout.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature`.
5. Open a Pull Request.

Please adhere to PEP 8 style guidelines and include tests for new features. Submit issues or feature requests via GitHub Issues.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by Django tutorials from the official documentation and sites like Real Python.
- Thanks to the Django community for packages like django-filters and Pillow.
- Special mention to open-source tools enabling educational projects.
