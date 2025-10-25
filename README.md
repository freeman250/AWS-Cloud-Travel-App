[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=19672436)

# Final Project

- **Title**: Cloud App Travel Journal  
- **Author**: Fred Junior Ntwali  

---

## Project Description

# 🌍 Cloud Travel Journal 📝  

### Overview  
**Cloud Travel Journal** is a cloud-native web application that allows users to document and share their travel experiences. Users can write journal entries, upload images or documents, and manage their memories through a sleek web interface—powered entirely by AWS cloud services.

---

## Features

✅ **Journal Entry Creation**  
- Add a title, story, and optionally upload an image (stored in S3).  
- Entries are stored in **DynamoDB** with timestamps.  

✅ **Gallery View**  
- Displays all travel entries with options to edit or delete them.  
- Embedded images are rendered from the S3 bucket.

✅ **Edit & Delete Support**  
- Update text or replace entries with ease.  
- Remove entries permanently via the UI.

✅ **Minimalistic and Functional UI**  
- Easy-to-navigate, clean layout built with HTML templates.  
- Designed to work within AWS-hosted environments like **Cloud9** or **Elastic Beanstalk**.

---

## Configuration Architecture

✅ **AWS Services Used**  
- **DynamoDB** – Stores journal entries as strings, with `id`, `title`, `entry`, `timestamp`, and optional `image_url`.  
- **S3 (Simple Storage Service)** – Stores uploaded images linked to each journal entry.  
- **EC2 (optional)** – Can also run the app manually with more control.

✅ **Technology Stack**  
- **Backend**: Python + Flask  
- **Frontend**: HTML (Jinja templates), optional Bootstrap for styling  
- **Cloud Storage**: AWS S3  
- **NoSQL Database**: AWS DynamoDB  
- **Development Environment**: AWS Cloud9  

---

## Folder Structure

```bash
.
├── app.py                 # Main Flask application
├── templates/
│   ├── home.html
│   ├── journal.html
│   ├── gallery.html
│   └── edit.html
├── static/                # Optional: add styles/images if needed
├── requirements.txt       # Flask + boto3 dependencies
└── README.md              # This file
