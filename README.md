 AI Memory Plan – An AI-Powered Digital Diary for Alzheimer’s & Memory Care

AI Memory Plan is an intelligent, multi-modal digital diary built to support Alzheimer’s patients, individuals with dementia, caregivers, and healthcare professionals in preserving memories, tracking emotional well-being, and analyzing cognitive patterns over time. Designed with accessibility and simplicity in mind, the system integrates Gradio, Hugging Face Transformers, Tesseract OCR, and SQLite, blending text, images, and AI analytics into one supportive memory-assist platform.

 Features

The AI Memory Plan offers a comprehensive suite of assistive tools.
The Memory Recording module enables users to write daily entries, upload images, extract text automatically through OCR, and save them with timestamps, weekday tags, emotion scores, and secure storage in SQLite with optional Google Drive backup. The Emotion Detection system uses a DistilBERT classifier capable of identifying six emotions, backed by a keyword-matching system with over 80 cues and sentiment polarity analysis via TextBlob to generate confidence-based emotional insights. The OCR System, powered by Tesseract, extracts text from images, removes noise, and merges extracted text with user-written entries for better context.

The Memory Library provides a chronological, searchable list of all memories with filters for date, emotion, or weekday, along with emotion badges, image previews, metadata, and CSV export support. The Analytics Dashboard visualizes emotional trends through bar, pie, and line charts, showing all-time mood patterns, frequent emotions, image-to-text ratios, and recent activity summaries. Meanwhile, the Calendar View displays an interactive monthly layout where memory-marked dates can be clicked to reveal entries.

Smart reminders allow scheduling of medications, mood check-ins, appointments, or custom tasks, with support for WhatsApp notifications via Twilio. The platform includes Multilingual Support for English, Hindi, Marathi, Spanish, and French, along with a Dynamic Theme System offering Happy, Calm, Energetic, and High-Contrast accessibility themes. Finally, a secure User System supports registration, login, password validation, personalized language settings, themes, and WhatsApp number setup.

 Tech Stack

The system uses a simple but powerful stack, including Gradio for the frontend UI, Python for backend processing, SQLite for persistent storage, Tesseract OCR for text extraction, DistilBERT and TextBlob for emotion analysis, Twilio WhatsApp API for reminders, and Matplotlib, Plotly, and Pandas for visualizations, with optional Google Drive integration for cloud persistence.

 Database Schema

The platform uses four structured tables:
Users (id, username, password, name, phone number, language, theme preference, created_at),
Memories (id, username, timestamp, weekday, date, text, predicted emotion, emotion scores in JSON, image path),
Reminders (id, username, title, description, reminder_date, reminder_time, type, completion status), and
Feedback (id, username, rating, comments, created_at).

 Installation & Setup

To set up the project, clone the repository, install required dependencies, and configure OCR. Tesseract can be installed via UB Mannheim builds on Windows, via apt install on Linux, or through Homebrew on macOS. For WhatsApp reminders, configure the Twilio SID, Auth Token, and WhatsApp number inside a .env file. Launch the app using python app.py and the interface will be available through the Gradio UI.

 Project Structure

The primary structure includes app.py, the SQLite database, model files, helper utilities, assets, requirements, and the main README — all organized cleanly under the project folder.

 Use Cases

The project benefits multiple groups:
For patients, it helps preserve memories, maintain emotional awareness, and track daily experiences.
For caregivers, it offers tools to monitor emotional shifts, schedule reminders, and observe behavioral patterns.
For healthcare professionals, it enables long-term emotional analytics, cognitive trend tracking, and access to research-friendly datasets supporting clinical studies.

 Future Enhancements

Planned additions include voice-to-text entries, facial emotion recognition, multi-caregiver support, AI-generated conversation prompts, wearable device integration, and video diary capabilities, allowing the platform to evolve into a more immersive support system.

 Ethical & Privacy Considerations

All user data is stored responsibly using local SQLite with optional encrypted paths, and users retain full control to delete or export their data at any time. The platform clearly communicates how AI is used and emphasizes that it is a supportive tool—not a medical diagnostic system. Privacy, accessibility, and transparency remain core design principles.
