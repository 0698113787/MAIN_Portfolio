# Portfolio Website

A professional portfolio website built with Flask, featuring a contact form with email notifications, resume showcase, certificates gallery, and testimonials section.

## Features

- **Home Page**: Introduction and overview
- **About**: Personal information and background
- **Resume**: Professional experience and skills
- **Certificates**: Gallery of certifications and achievements
- **Testimonials**: Client and colleague recommendations
- **Contact Form**: Functional feedback form with email notifications

  ## 🌐 Live Demo

**[View Live Portfolio](https://main-portfolio-one-beige.vercel.app/home)**

## Tech Stack

- **Backend**: Flask (Python)
- **Email**: Flask-Mail with Gmail SMTP
- **Frontend**: HTML, CSS , JavaScripts
- **Deployment**: Vercel-ready configuration

## Project Structure

```
MyPortfolio/
├── static/
│   ├── about.css
│   ├── certificates.css
│   ├── feedback.css
│   ├── header.css
│   ├── home.css
│   ├── login.css
│   ├── resume.css
│   ├── sent.css
│   ├── fail.css
│   ├── testimonials.css
│   ├── mycv.pdf
│   ├── andile.jpeg
│   ├── bro_lungisani_po.jpeg
│   ├── sbani_po.jpeg
│   ├── cyber_cerificates.jpeg
│   └── Mobile_certificates.jpeg
├── templates/
│   ├── about.html
│   ├── certificates.html
│   ├── feedback.html
│   ├── fail.html
│   ├── header.html
│   ├── resume.html
│   ├── sent.html
│   └── testimonials.html
├── app.py
├── requirements.txt
├── vercel.json
```

## Installation

### Prerequisites

- Python 3.8+
- pip
- Gmail account with App Password

### Setup
1. **Create a virtual environment**
   ```bash
   python -m venv venv
   
   # Windows
   venv\Scripts\activate
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   SECRET_KEY=your_secret_key_here
   GMAIL_USER=your_email@gmail.com
   GMAIL_APP_PASSWORD=your_gmail_app_password
   ```

   **To get Gmail App Password:**
   - Go to your Google Account settings
   - Enable 2-Factor Authentication
   - Go to Security > 2-Step Verification > App passwords
   - Generate a new app password for "Mail"
   - Copy the 16-character password to your `.env` file

4. **Run the application**
   ```bash
   python -m flask run
   python app.py
   ```
   
   Visit `http://localhost:5000` in your browser

## Configuration

### Email Setup

The contact form uses Gmail SMTP. Configure these settings in your `.env` file:

- `GMAIL_USER`: Your Gmail address
- `GMAIL_APP_PASSWORD`: Gmail App Password (not your regular password)

### Testing Email

Visit `/test-email` to verify your email configuration is working correctly.

### Health Check

Visit `/health` to check the application status and email configuration.

## Deployment

### Vercel Deployment

This project is configured for Vercel deployment with the included `vercel.json` file.

1. **Deploy**
   ```bash
   vercel.com
   ```

2. **Add Environment Variables**
   
   In Vercel dashboard, add:
   - `SECRET_KEY`
   - `GMAIL_USER`
   - `GMAIL_APP_PASSWORD`

## Routes

- `/` or `/home` - Home page
- `/about` - About page
- `/resume` - Resume/CV
- `/certificates` - Certificates gallery
- `/testimonials` - Testimonials section
- `/feedback` - Contact form
- `/sent` - Success confirmation page
- `/fail` - Error page
- `/test-email` - Email configuration test
- `/health` - Application health check

## Contact Form Flow

1. User fills out the form with name, email, subject, and message
2. Form data is validated
3. Email is sent to My Gmail address
4. User is redirected to success or failure page
5. I receive a formatted email with the contact details

## Troubleshooting

### Email not sending

1. Verify Gmail credentials in `.env`
2. Check that 2FA is enabled on your Google account
3. Ensure you're using an App Password, not your regular password
4. Test with `/test-email` endpoint
5. Check console logs for error messages


## Security Notes

- Never commit `.env` file to version control
- Keep your `GMAIL_APP_PASSWORD` secret
- Use strong `SECRET_KEY` in production
- Add `.env` to `.gitignore`


---


## 👤 Author

**Andile Ntshangase**
- Email: vuyiswaandile176@gmail.com
- 
**Built with ❤️ using Flask**
