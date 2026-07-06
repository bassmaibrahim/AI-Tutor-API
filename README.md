# 📚 AI Tutor API

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi)
![Gemini](https://img.shields.io/badge/Google-Gemini_2.5_Flash-4285F4?style=for-the-badge&logo=google)
![Groq](https://img.shields.io/badge/Groq-Llama_3.3_70B-black?style=for-the-badge)
![Flutter](https://img.shields.io/badge/Flutter-Mobile_App-02569B?style=for-the-badge&logo=flutter)
![Firebase](https://img.shields.io/badge/Firebase-Cloud-orange?style=for-the-badge&logo=firebase)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

</p>

---

# 📖 Overview

**AI Tutor API** is an intelligent educational backend built with **FastAPI** that powers the AI Tutor inside a Flutter mobile learning application.

The system allows students to upload educational documents and automatically transforms them into interactive learning resources using **Large Language Models (LLMs)**.

Instead of simply summarizing documents, the AI Tutor creates a complete learning experience by generating:

- 📄 AI Summary
- 📌 Key Points
- 💡 Simple Explanations
- ❓ Quiz Questions
- 💬 Question & Answer Pairs
- 🎥 Related YouTube Learning Videos

The backend communicates with the Flutter application through REST APIs, while the mobile app provides authentication, course management, and **Text-to-Speech (TTS)** to read AI-generated content aloud.

---

# 🎯 Project Goals

The AI Tutor was designed to help students learn more efficiently by converting static educational documents into interactive study materials.

The system aims to:

- Reduce study time.
- Improve concept understanding.
- Encourage self-learning.
- Generate revision materials automatically.
- Recommend additional learning resources.
- Support accessible learning through Text-to-Speech.

---

# ✨ Features

| Feature | Description |
|----------|-------------|
| 🔍 Smart Document Validation | Validates file type, size, and educational content before processing. |
| 📄 Document Extraction | Extracts text from PDF, DOCX, and TXT files. |
| 📝 AI Summarization | Generates concise summaries from uploaded documents. |
| 📌 Key Point Extraction | Highlights the most important concepts for quick revision. |
| 💡 AI Explanation | Explains difficult topics in a simple, student-friendly way. |
| ❓ Quiz Generation | Automatically creates quiz questions from lesson content. |
| 💬 Question & Answer Generation | Generates intelligent Q&A pairs for revision and self-assessment. |
| 🎥 YouTube Recommendation | Recommends educational YouTube videos related to the detected topic. |
| 🔍 Topic Detection | Identifies the document's primary subject automatically. |
| 📱 Flutter Integration | Exposes REST APIs consumed by the Flutter mobile application. |
| 🔊 Text-to-Speech Support | AI-generated summaries and explanations can be read aloud through the Flutter app. |

---

# 🤖 AI Capabilities

The AI Tutor can automatically:

- ✅ Validate uploaded documents
- ✅ Detect educational content
- ✅ Extract document text
- ✅ Detect lesson topic
- ✅ Generate concise summaries
- ✅ Extract key points
- ✅ Explain complex concepts
- ✅ Generate quizzes
- ✅ Generate question-answer pairs
- ✅ Recommend educational YouTube videos
- ✅ Return structured JSON responses for the Flutter application
- ✅ Support accessible learning through Flutter Text-to-Speech integration

---

# 🏗️ System Architecture

```text
                     ┌─────────────────────┐
                     │ Flutter Mobile App  │
                     │ (Teacher & Student) │
                     └──────────┬──────────┘
                                │
                         REST API Requests
                                │
                                ▼
                     ┌─────────────────────┐
                     │     FastAPI API     │
                     └──────────┬──────────┘
                                │
        ┌───────────────────────┼─────────────────────────┐
        │                       │                         │
        ▼                       ▼                         ▼
 Smart Filter            AI Processing           YouTube Search
   (Groq)                 (Gemini)                 (Google API)

        │                       │
        │                       │
        ▼                       ▼
 Document Validation      Summary
                          Key Points
                          Explanation
                          Quiz
                          Q&A
                          Topic Detection

                │
                ▼

      Structured JSON Response

                │
                ▼

      Flutter AI Tutor Module

                │
        ┌───────┴────────┐
        │                │
        ▼                ▼
   Display Results   Text-to-Speech
```

---

# ⚙️ AI Processing Pipeline

```text
Upload Document
        │
        ▼
Smart Validation
        │
        ▼
Document Text Extraction
        │
        ▼
Educational Content Detection
        │
        ▼
Topic Detection
        │
        ▼
AI Processing
   ├── Summary
   ├── Key Points
   ├── Explanation
   ├── Quiz Generation
   ├── Question & Answer Generation
   └── Learning Enhancement
        │
        ▼
YouTube Recommendation
        │
        ▼
REST API Response
        │
        ▼
Flutter Mobile Application
        │
        ├── Display AI Content
        └── Text-to-Speech Playback
```

---

# 🛠️ Technologies Used

| Category | Technologies |
|-----------|--------------|
| Backend | FastAPI, Python |
| AI Models | Gemini 2.5 Flash, Groq Llama 3.3 70B |
| APIs | YouTube Data API v3 |
| Mobile | Flutter |
| Database | Firebase Firestore |
| Authentication | Firebase Authentication |
| Storage | Firebase Storage |
| Text Processing | PyMuPDF, python-docx |
| Deployment | Uvicorn |
---

# 🔑 API Keys

The AI Tutor API uses **three external services** to provide intelligent educational features.

| Service | Purpose |
|----------|----------|
| **Groq API** | Educational content validation and document filtering |
| **Google Gemini API** | AI summarization, explanations, quizzes, Q&A generation, and key point extraction |
| **YouTube Data API v3** | Educational video recommendations |

> ⚠️ **Important**
>
> Never commit your API keys to GitHub. Store them securely in your `.env` file.

---

# 📥 Getting API Keys

## 1️⃣ Groq API

**Purpose**

- Smart Document Filter
- Educational Content Classification
- Topic Validation

### Steps

1. Visit **https://console.groq.com**
2. Create a free account.
3. Open **API Keys**.
4. Click **Create API Key**.
5. Copy your key.

Example

```
gsk_xxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## 2️⃣ Google Gemini API

**Purpose**

- AI Summary
- Key Points
- AI Explanation
- Quiz Generation
- Question & Answer Generation

### Steps

1. Visit **https://aistudio.google.com**
2. Login using your Google account.
3. Click **Get API Key**.
4. Select **Create API Key**.
5. Copy the generated key.

Example

```
AIxxxxxxxxxxxxxxxxxxxxxxxxxx
```

> ⚠️ Free Tier
>
> - 5 requests/minute
> - 20 requests/day
>
> The application automatically handles rate limiting.

---

## 3️⃣ YouTube Data API

**Purpose**

- Educational video recommendations

### Steps

1. Visit **https://console.cloud.google.com**
2. Create a new project.
3. Enable **YouTube Data API v3**.
4. Navigate to

```
APIs & Services
        ↓
Credentials
        ↓
Create Credentials
        ↓
API Key
```

5. Copy the generated key.

Example

```
AIzaxxxxxxxxxxxxxxxxxxxxxxxx
```

> Free quota:
>
> **100 search units/day**

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/AI-Tutor-Backend.git

cd AI-Tutor-Backend
```

---

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### Windows Users

If you encounter an error while installing **python-magic**, run:

```bash
pip install python-magic-bin
```

---

# 🌍 Environment Variables

Create a `.env` file in the project root.

Example

```env
GROQ_API_KEY=gsk_your_key_here

GEMINI_API_KEY=AI_your_key_here

YOUTUBE_API_KEY=AIza_your_key_here
```

Your project structure should now look like:

```
AI-Tutor-Backend/

│── .env
│── .env.example
│── requirements.txt
│── app/
```

---

# ▶️ Run the Application

Start the FastAPI server:

```bash
uvicorn app.main:app --reload
```

By default, the API will run at

```
http://127.0.0.1:8000
```

---

# 📖 API Documentation

FastAPI automatically generates interactive API documentation.

### Swagger UI

```
http://127.0.0.1:8000/docs
```

Interactive testing for every endpoint is available directly in the browser.

---

### ReDoc Documentation

```
http://127.0.0.1:8000/redoc
```

Provides a clean, documentation-style view of the API.

---

# ✅ Verify Installation

If everything is configured correctly, opening

```
http://127.0.0.1:8000/docs
```

should display the available endpoints:

- ✅ Document Validation
- ✅ AI Processing
- ✅ Summary Generation
- ✅ Key Point Extraction
- ✅ AI Explanation
- ✅ Quiz Generation
- ✅ Question & Answer Generation
- ✅ YouTube Recommendations

---

# 📦 Dependencies

Main libraries used in the project include:

- FastAPI
- Uvicorn
- Pydantic
- python-dotenv
- Groq SDK
- Google Generative AI SDK
- PyMuPDF
- python-docx
- python-magic
- Requests

Install all dependencies using:

```bash
pip install -r requirements.txt
```
---

# 📁 Project Structure

```
AI-Tutor-Backend/
│
├── .env                         # Environment variables (Not committed)
├── .env.example                 # Environment variable template
├── requirements.txt             # Project dependencies
├── README.md                    # Project documentation
│
└── app/
    │
    ├── main.py                  # FastAPI application entry point
    │
    ├── api/
    │   └── routes.py            # REST API endpoints
    │
    ├── core/
    │   ├── config.py            # Application configuration
    │   └── schemas.py           # Request & Response models
    │
    ├── services/
    │   ├── extractor_service.py
    │   ├── filter_service.py
    │   ├── summarizer_service.py
    │   ├── explanation_service.py
    │   ├── quiz_service.py
    │   ├── qa_service.py
    │   └── youtube_service.py
    │
    └── utils/
        └── helpers.py           # Shared helper functions
```

---

# 📂 Folder Description

### 📌 app/api

Contains all REST API endpoints exposed to the Flutter application.

Responsibilities:

- Receive uploaded documents.
- Validate incoming requests.
- Call AI services.
- Return structured JSON responses.

---

### 📌 app/core

Contains the application's configuration and shared schemas.

Includes:

- Environment variables
- API keys
- Pydantic models
- Response schemas

---

### 📌 app/services

The business logic of the application.

Each AI feature is isolated into its own service to improve maintainability and scalability.

Current services include:

| Service | Responsibility |
|----------|----------------|
| Extractor Service | Extracts text from uploaded documents |
| Filter Service | Detects educational content and validates uploaded files |
| Summarizer Service | Generates AI summaries |
| Explanation Service | Produces student-friendly explanations |
| Quiz Service | Generates quiz questions |
| QA Service | Generates question-answer pairs |
| YouTube Service | Finds educational videos related to the detected topic |

---

### 📌 app/utils

Contains helper functions shared across multiple services.

Examples:

- File utilities
- Text preprocessing
- Common validation
- Helper methods

---

# 🏛 System Design

The project follows a modular service-oriented architecture.

```
Flutter Mobile App
        │
        ▼
FastAPI Routes
        │
        ▼
Business Services
        │
        ├──────────────┐
        │              │
        ▼              ▼
Document        AI Processing
Extraction
        │
        ▼
Educational Filter
        │
        ▼
Topic Detection
        │
        ▼
Content Generation
        │
        ├── Summary
        ├── Key Points
        ├── Explanation
        ├── Quiz
        ├── Q&A
        └── YouTube Recommendation
        │
        ▼
JSON Response
```

---

# 🔄 Request Flow

The following diagram illustrates how a document is processed.

```
Student uploads document
            │
            ▼
Receive Request
            │
            ▼
Validate File

 ├── File Type
 ├── File Size
 └── Educational Content

            │
            ▼

Extract Document Text

            │
            ▼

Detect Topic

            │
            ▼

Gemini Processing

 ├── Summary
 ├── Key Points
 ├── Explanation
 ├── Quiz
 └── Question & Answers

            │
            ▼

Search YouTube API

            │
            ▼

Combine Results

            │
            ▼

Return JSON Response

            │
            ▼

Flutter Mobile Application

            │
      ┌─────┴───────────┐
      ▼                 ▼

Display Content     Text-to-Speech
```

---

# 🧠 AI Workflow

The backend follows a multi-stage AI pipeline.

## Stage 1 — Validation

The uploaded file is checked for:

- Supported file type
- Maximum file size
- Minimum word count
- Educational content
- Harmful or unsafe content

Only approved documents continue to AI processing.

---

## Stage 2 — Text Extraction

The backend extracts raw text from:

- PDF
- DOCX
- TXT

The extracted content is cleaned before being sent to the AI model.

---

## Stage 3 — Topic Detection

The system automatically identifies the document's main topic.

Example:

```
Computer Networks

Machine Learning

Embedded Systems

Operating Systems

Data Structures
```

The detected topic is later used to improve YouTube recommendations.

---

## Stage 4 — AI Content Generation

Google Gemini generates multiple learning resources simultaneously.

Generated outputs include:

- 📄 Summary
- 📌 Key Points
- 💡 Simple Explanation
- ❓ Quiz Questions
- 💬 Question & Answer Pairs

---

## Stage 5 — Educational Video Recommendation

The detected topic is sent to the YouTube Data API.

The backend retrieves:

- Relevant videos
- Channel names
- Thumbnails
- Video URLs
- Descriptions

---

## Stage 6 — Response Formatting

All generated content is merged into a single structured JSON response.

The Flutter application receives one response containing every AI-generated learning resource.

---

# 🎯 Design Principles

This project was designed following software engineering best practices.

### ✅ Separation of Concerns

Each AI task is implemented in an independent service.

---

### ✅ Scalability

New AI features can be added without modifying existing services.

Examples:

- Flashcards
- Mind Maps
- Learning Paths
- Translation
- Assignment Generator

---

### ✅ Maintainability

Business logic is separated from API routes, making the project easier to test and maintain.

---

### ✅ Reusability

Each service can be reused independently by other applications through the REST API.
---

# 🚀 API Documentation

The AI Tutor Backend exposes RESTful APIs that allow the Flutter application to upload educational documents and receive AI-generated learning content.

**Base URL**

```
http://127.0.0.1:8000
```

---

# 📌 Available Endpoints

| Method | Endpoint | Description |
|----------|-----------------|--------------------------------|
| POST | `/api/v1/filter` | Validate uploaded document |
| POST | `/api/v1/process` | Full AI processing pipeline |

---

# 📄 POST `/api/v1/filter`

Validates the uploaded document before AI processing.

The endpoint checks:

- Supported file type
- Maximum file size
- Minimum word count
- Educational content
- Unsafe content

If validation succeeds, the document can be processed by the AI Tutor.

---

## Request

### Content Type

```
multipart/form-data
```

### Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| file | File | ✅ Yes | PDF, DOCX or TXT document |

---

## Example Request

```
POST /api/v1/filter
```

Upload

```
embedded_systems.pdf
```

---

## Success Response

```json
{
  "status": "approved",
  "message": "Document passed all validation checks.",
  "word_count": 2538,
  "detected_topic": "Embedded Systems",
  "confidence": 0.96
}
```

---

## Rejected Response

```json
{
    "status":"rejected",
    "reason":"not_educational_content"
}
```

---

# 📚 POST `/api/v1/process`

Processes an educational document through the complete AI pipeline.

The backend performs:

- Document Validation
- Text Extraction
- Topic Detection
- Summary Generation
- Key Point Extraction
- AI Explanation
- Quiz Generation
- Question & Answer Generation
- YouTube Recommendation

All generated content is returned in a single JSON response.

---

## Request

### Content Type

```
multipart/form-data
```

---

## Parameters

| Parameter | Type | Default | Description |
|------------|----------|---------|--------------------------------|
| file | File | — | Uploaded document |
| include_summary | Boolean | true | Generate AI summary |
| include_key_points | Boolean | true | Extract key points |
| include_explanation | Boolean | true | Generate explanation |
| include_quiz | Boolean | true | Generate quiz questions |
| include_qa | Boolean | true | Generate Q&A pairs |
| include_youtube | Boolean | true | Recommend YouTube videos |
| num_questions | Integer | 5 | Number of quiz/Q&A questions |
| num_videos | Integer | 5 | Number of YouTube videos |

---

## Example Request

```
POST /api/v1/process
```

Query Parameters

```
include_summary=true

include_key_points=true

include_explanation=true

include_quiz=true

include_qa=true

include_youtube=true

num_questions=5

num_videos=5
```

---

# 📤 Example Response

```json
{
  "word_count": 2538,

  "detected_topic": "Embedded Systems",

  "confidence": 0.96,

  "summary": {
    "summary": "Embedded systems are specialized computing systems designed to perform dedicated tasks.",

    "key_points": [
      "Microcontrollers are widely used.",
      "Memory optimization is important.",
      "Real-time processing is essential.",
      "C programming dominates embedded development.",
      "Power efficiency is a key requirement."
    ]
  },

  "explanation": {
    "content": "Think of an embedded system as a small computer built inside another device. Unlike your laptop, it performs one specific task such as controlling a washing machine or a car engine."
  },

  "quiz": {
    "total": 5,
    "questions": [
      {
        "question": "Why is C commonly used in embedded systems?",
        "options": [
          "A. Faster development",
          "B. Hardware control",
          "C. Better graphics",
          "D. Database support"
        ],
        "answer": "B"
      }
    ]
  },

  "qa": {
    "total": 5,
    "qa_pairs": [
      {
        "question": "What is an embedded system?",
        "answer": "A computer designed for a dedicated function inside a larger device."
      }
    ]
  },

  "youtube": {
    "total": 5,
    "search_query": "Embedded Systems",

    "videos": [
      {
        "title": "Embedded Systems Full Course",

        "url": "https://www.youtube.com/watch?v=...",

        "channel": "Neso Academy",

        "thumbnail": "...",

        "description": "Complete embedded systems course."
      }
    ]
  }
}
```

---

# ⚠️ Error Responses

## Invalid File Type

```json
{
    "status":"rejected",
    "reason":"invalid_file_type"
}
```

---

## File Too Large

```json
{
    "status":"rejected",
    "reason":"file_too_large"
}
```

---

## Content Too Short

```json
{
    "status":"rejected",
    "reason":"content_too_short"
}
```

---

## Non-Educational Document

```json
{
    "status":"rejected",
    "reason":"not_educational_content"
}
```

---

## Unsafe Content

```json
{
    "status":"rejected",
    "reason":"unsafe_content"
}
```

---

# 📋 HTTP Status Codes

| Status Code | Meaning |
|-------------|--------------------------------|
| 200 | Request processed successfully |
| 400 | Invalid request |
| 401 | Unauthorized |
| 404 | Endpoint not found |
| 413 | Uploaded file exceeds maximum size |
| 422 | Validation error |
| 500 | Internal server error |

---

# 🧪 Testing the API

After running the server, open:

```
http://127.0.0.1:8000/docs
```

FastAPI automatically generates interactive Swagger documentation where every endpoint can be tested directly from the browser.

Alternatively,

```
http://127.0.0.1:8000/redoc
```

provides a cleaner documentation interface.

---

# 📱 Flutter Integration

The Flutter mobile application communicates with the backend through REST APIs.

Typical workflow:

```
Student uploads lesson

        │

        ▼

Flutter sends multipart/form-data request

        │

        ▼

FastAPI processes document

        │

        ▼

Gemini + Groq + YouTube APIs

        │

        ▼

Structured JSON response

        │

        ▼

Flutter displays:

• Summary

• Key Points

• Explanation

• Quiz

• Question & Answers

• YouTube Videos

        │

        ▼

Flutter Text-to-Speech reads generated content aloud
```
---

# 📂 Supported File Types

The AI Tutor currently supports the following document formats:

| File Type | Extension | Maximum Size |
|------------|-----------|--------------|
| PDF | `.pdf` | 50 MB |
| Microsoft Word | `.docx` | 50 MB |
| Plain Text | `.txt` | 50 MB |

> Files that exceed the maximum size or use unsupported formats will be rejected before AI processing.

---

# ❌ Validation & Rejection Reasons

Before processing a document, the Smart Filter performs several validation checks.

| Reason | Description |
|----------|-------------|
| `invalid_file_type` | Uploaded file is not PDF, DOCX, or TXT |
| `file_too_large` | File exceeds the maximum allowed size |
| `content_too_short` | Document contains insufficient text |
| `not_educational_content` | Document is not educational |
| `unsafe_content` | Harmful or unsafe content detected |

Example response

```json
{
    "status":"rejected",
    "reason":"not_educational_content"
}
```

---

# 🛠️ Tech Stack

## Backend

- Python
- FastAPI
- Uvicorn
- Pydantic

---

## AI & Machine Learning

- Google Gemini 2.5 Flash
- Groq (Llama 3.3 70B)

---

## External APIs

- YouTube Data API v3

---

## Document Processing

- PyMuPDF
- python-docx
- python-magic

---

## Mobile Application

- Flutter
- Firebase Authentication
- Firebase Firestore
- Firebase Storage
- Text-to-Speech (Flutter TTS)

---

## Development Tools

- Git
- GitHub
- VS Code
- Postman

---

# 📷 Screenshots

## Flutter Application

### Login

> *(Add Screenshot)*

---

### Student Dashboard

> *(Add Screenshot)*

---

### Teacher Dashboard

> *(Add Screenshot)*

---

### Upload Lesson

> *(Add Screenshot)*

---

### AI Summary

> *(Add Screenshot)*

---

### AI Explanation

> *(Add Screenshot)*

---

### Quiz Generation

> *(Add Screenshot)*

---

### Question & Answer

> *(Add Screenshot)*

---

### YouTube Recommendations

> *(Add Screenshot)*

---

### Text-to-Speech

> *(Add Screenshot)*

---

### Swagger Documentation

> *(Add Screenshot)*

---

# 🚀 Future Improvements

The project can be extended with additional AI-powered educational features.

Planned improvements include:

- 🧠 Flashcard Generation
- 🗺️ Mind Map Generation
- 📚 Personalized Study Plans
- 🌍 Multi-language Support
- 🎙️ Voice-based AI Tutor
- 💬 Conversational AI Chatbot
- 📊 Student Learning Analytics
- 📝 Assignment Generator
- 📖 Lesson Translation
- 🧩 Adaptive Difficulty Quizzes
- 📅 Smart Revision Scheduler
- 🎓 AI Learning Recommendations

---

# 🔒 Security

The project follows basic security practices:

- API keys stored in environment variables
- `.env` excluded from Git
- File validation before processing
- Request validation using Pydantic
- Secure REST API communication
- Input sanitization before AI processing

---

# ⚡ Performance

The backend is optimized to:

- Validate documents before AI requests
- Reduce unnecessary API calls
- Minimize response latency
- Handle large educational documents efficiently
- Return structured JSON for easy Flutter integration

---

# 📖 Example Workflow

```text
Teacher uploads lesson
          │
          ▼
Student joins class
          │
          ▼
Student opens lesson
          │
          ▼
Student uploads document
          │
          ▼
AI Tutor Backend
          │
          ├── Validate Document
          ├── Extract Text
          ├── Detect Topic
          ├── Generate Summary
          ├── Generate Key Points
          ├── Explain Concepts
          ├── Generate Quiz
          ├── Generate Q&A
          └── Recommend Videos
          │
          ▼
Flutter App
          │
          ├── Display Results
          ├── Save Progress
          └── Read Content with Text-to-Speech
```

---

# 🤝 Contributing

Contributions are welcome!

If you'd like to improve the project:

1. Fork the repository.
2. Create a new feature branch.

```bash
git checkout -b feature/new-feature
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push your branch.

```bash
git push origin feature/new-feature
```

5. Open a Pull Request.

---

# 👨‍💻 Author

**Bassma Ibrahim**

Machine Learning Engineer • Data Scientist • AI Engineer

- GitHub: https://github.com/bassmaibrahim
- LinkedIn: https://www.linkedin.com/in/bassma-ibrahim/

---

# 🙏 Acknowledgements

Special thanks to:

- Google Gemini
- Groq
- FastAPI
- Flutter
- Firebase
- YouTube Data API
- Open-source AI community

for providing the tools and technologies that made this project possible.

---

# 📄 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project for educational and personal purposes.

See the `LICENSE` file for more information.

---

# ⭐ Support

If you found this project useful:

⭐ Star the repository

🍴 Fork the project

🐞 Report issues

💡 Suggest new features

Your support helps improve the project and motivates future development.
