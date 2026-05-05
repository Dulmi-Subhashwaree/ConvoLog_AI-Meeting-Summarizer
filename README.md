# ConvoLog – AI Meeting Summarizer

<p align="center">
  <img src="Convolog_Logo.png" alt="Convolog" width="300"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.13-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-1.49-FF4B4B?logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/Gemini-2.5%20Flash-4285F4?logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/License-Academic-yellow" />
</p>

---

## Overview

**ConvoLog** is an AI-powered web application designed to convert unstructured meeting data into clear, structured summaries.
The system supports multiple input formats including text, documents, audio, and images, and uses AI to extract key insights and present them in an organized manner.

Built using **Python** and **Streamlit**, ConvoLog integrates the **Google Gemini 2.5 Flash** large language model to intelligently process and summarize meeting content. The application provides a clean, modern interface with dark and light mode support, voice recording with live waveform visualization, and downloadable PDF reports.

---

## Objectives

- Summarize unstructured meeting conversations into structured outputs
- Convert audio recordings into text and generate summaries
- Extract key points from uploaded documents and scanned images
- Provide downloadable structured outputs in PDF format
- Improve productivity and information clarity for individuals and teams
- Support multiple input methods to suit different user workflows

---

## Technologies Used

| Technology | Version | Purpose |
|---|---|---|
| **Python** | 3.13 | Core programming language |
| **Streamlit** | 1.49 | Web application framework |
| **Google Gemini API** (google-genai) | Latest | AI summarization and image reading |
| **PyPDF2** | Latest | Extract text from PDF files |
| **python-docx** | Latest | Extract text from Word documents |
| **SpeechRecognition** | Latest | Transcribe audio files to text |
| **Pydub** | Latest | Audio format conversion (MP3 to WAV) |
| **ReportLab** | Latest | Generate downloadable PDF summaries |
| **ffmpeg** | Latest | Backend audio processing engine |
| **Web Speech API** | Browser | Real-time voice recording |
| **HTML5 Canvas** | Browser | Live audio waveform visualization |

---

## System Components

### Text Processing Module
Accepts raw text input pasted directly by the user or captured through live voice recording. Includes filler word removal and text cleaning before sending to the AI engine.

### Document Processing Module
Handles `.txt`, `.pdf`, and `.docx` file uploads. Extracts raw text content from each format using PyPDF2 and python-docx, then passes it to the summarization engine.

### Audio Processing Module
Accepts `.mp3` and `.wav` audio file uploads. Uses Pydub and ffmpeg to convert audio formats, then transcribes speech to text using the SpeechRecognition library with Google Speech API.

### Image Processing Module
Accepts JPG, PNG, WEBP, and BMP image uploads, as well as live camera capture. Uses Google Gemini Vision to read handwritten or printed text directly from images and generate summaries.

### AI Summarization Engine
The core of the application. Sends cleaned and structured prompts to the Google Gemini 2.5 Flash model with user-defined parameters for length, tone, and format. Parses the structured response into five output sections.

###
