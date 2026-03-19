# Rise-Internship-Project-7
Chatbot – Dialogflow Integration

# FarmCare Chatbot – Dialogflow Integration

## Project Overview

This project demonstrates how to build and deploy an AI-powered chatbot using Dialogflow and integrate it into a website.

The chatbot provides assistance for livestock health, including disease guidance, veterinary consultation help, and general FAQs.

---

## Features

* AI-powered chatbot using Dialogflow
* Handles user queries related to livestock health
* Embedded into a web page using Dialogflow Messenger
* Responsive UI with floating chatbot interface
* Real-time responses

---

## Tech Stack

* Frontend: HTML, CSS
* Chatbot Platform: Dialogflow
* Deployment: Static hosting (AWS S3, Netlify, GitHub Pages)

---

## Project Structure

```
FarmCare-Chatbot/
│── index.html
│── README.md
```

---

## Setup Instructions

### 1. Create Dialogflow Agent

* Open Dialogflow Console
* Create a new agent (e.g., FarmCareBot)
* Set default language to English

---

### 2. Create Intents

#### Default Welcome Intent

Response:

```
Hello! How can I help you today?
```

#### Custom Intent: Disease Help

Training phrases:

```
My cow is sick
Symptoms in cattle
Animal not eating
```

Response:

```
Please describe the symptoms or upload an image in our app for better diagnosis.
```

---

### 3. Integrate Chatbot into Website

Add the following code to the index.html file:

```html
<script src="https://www.gstatic.com/dialogflow-console/fast/messenger/bootstrap.js?v=1"></script>

<df-messenger
  intent="WELCOME"
  chat-title="FarmCareBot"
  agent-id="YOUR-AGENT-ID"
  language-code="en"
></df-messenger>
```

Replace YOUR-AGENT-ID with the Dialogflow agent ID.

---

### 4. Run Locally

```bash
python -m http.server 8000
```

Open in browser:

```
http://localhost:8000
```



## Testing

Use the Dialogflow console test panel to verify chatbot responses:

```
hi
my cow is sick
```

---
## Screenshots
<img width="1919" height="968" alt="Image" src="https://github.com/user-attachments/assets/bca71be9-d996-4bbb-95e9-7881a6bf3c54" />
<br><br>
<img width="855" height="1016" alt="Image" src="https://github.com/user-attachments/assets/d7c31049-7e68-4c12-80c8-e9a8c1b36f71" />
<br><br>
<img width="1919" height="1015" alt="Image" src="https://github.com/user-attachments/assets/b6e89c39-8365-4165-9db4-0203b900665a" />
<br><br>

---
## Future Enhancements

* Multi-language support (Tamil)
* Integration with AI-based disease prediction system
* Backend integration using FastAPI and webhooks
* User interaction tracking and analytics

