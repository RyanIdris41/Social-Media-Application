# Social Network Platform

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Architecture](#architecture)
- [Setup Guide](#setup-guide)
- [Configuration](#configuration)
- [Usage](#usage)
- [License](#license)

---

## Overview

This platform is a cutting-edge social network built to offer secure and efficient user interactions. Leveraging the MERN (MongoDB, Express.js, React.js, Node.js) stack, it provides key functionalities for social connectivity and advanced moderation tools. Highlights include:

1. AI-driven content moderation.
2. Context-based user authentication.
3. Rich user engagement features like profiles, posts, and interactions.

---

## Features

### Core Features
- Secure user registration and login with JWT.
- Comprehensive profile management.
- Post creation, editing, and sharing.
- Interactive features like commenting and liking.
- Reporting of inappropriate content.

### Advanced Features
- **Automated Content Moderation:**
  - Employs APIs such as Perspective API, TextRazor, and a custom Flask-based AI classifier.
  - Modular integration for flexibility in moderation tools.
- **Context-Based Authentication:**
  - Uses IP, location, and device data for secure logins.
  - Encrypts sensitive information with AES.
  - Sends email alerts for unusual login attempts.

### Role Management
- **Administrators:**
  - Control platform settings, oversee moderators, and manage flagged content.
- **Moderators:**
  - Monitor community activity and handle reported posts.
- **Users:**
  - Engage with content and manage personal profiles.

---

## Technology Stack

### Frontend
- React.js
- Redux for global state management
- Tailwind CSS for responsive design

### Backend
- Node.js with Express.js
- MongoDB for database management
- Authentication via JWT and Passport.js
- AES for encryption
- Nodemailer for email services

### Supporting Tools
- Azure Blob Storage for file handling
- Flask API with PyTorch for NLP tasks
- APIs like Perspective API, TextRazor, and Hugging Face Transformers

---

## Architecture

The platform adopts a modular design for scalability and clarity. The main components include:

1. **Frontend:** A single-page application for user interaction, built with React.
2. **Backend:** API server in Node.js for processing logic and database operations.
3. **Database:** MongoDB for storing structured data.
4. **Moderation Engine:** Flask-based AI integration for content review.

---

## Setup Guide

### Prerequisites
- Node.js and npm
- MongoDB (local or cloud)

### Installation Steps

1. Clone the repository:

   ```bash
   git clone (https://github.com/RyanIdris41/Social-Media-Application.git)
   ```

2. Navigate to the project folder:

   ```bash
   cd project-folder
   ```

3. Install dependencies for client and server:

   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

4. Configure environment variables:

   - Create `.env` files in `client` and `server` directories.
   - Refer to `.env.example` for the required variables.

5. Start the backend:

   ```bash
   cd server
   npm start
   ```

6. Start the frontend:

   ```bash
   cd client
   npm start
   ```

---

## Configuration

### Admin Tool
Run the `admin_tool.sh` script to set up essential configurations:

- Create admin accounts.
- Initialize platform settings.

```bash
chmod +x admin_tool.sh
./admin_tool.sh
```

### Environment Variables

#### Email Notifications
```bash
EMAIL=<your-email>
PASSWORD=<your-email-password>
EMAIL_SERVICE=<email-provider>
```

#### Content Moderation
Obtain API keys for:

- [Perspective API](https://developers.perspectiveapi.com/s/docs-get-started)
- [TextRazor](https://www.textrazor.com/)
- [Hugging Face](https://huggingface.co/)

Optionally, use the Flask-based classifier as a local alternative.

---

## Usage

### Admins
- Access the admin dashboard at `/admin`.
- Manage moderators and platform configurations.

### Moderators
- Review reported content and oversee user interactions.

### Users
- Create and engage with posts, comments, and other users.

---

## License

This project is licensed under the MIT License. Check the `LICENSE` file for details.
