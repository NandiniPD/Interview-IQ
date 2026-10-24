# InterviewIQ

An interview-preparation suite with separate experiences for general interview practice, aptitude tests, and HR interview simulations. The repository contains three React frontends and two Express APIs, launched together from the repository root.

## Applications

| App | Description | URL |
| --- | --- | --- |
| InterviewIQ | Interview preparation dashboard with Firebase authentication | http://localhost:3000 |
| Aptitude | Aptitude practice and timed tests | http://localhost:3001 |
| HR Interview | HR interview practice and feedback | http://localhost:3002 |

The HR API runs on port `5000`; the Aptitude API runs on port `5001`.

## Requirements

- [Node.js](https://nodejs.org/) and npm
- Git
- A Firebase project for signing in to the InterviewIQ app

## Configure Firebase

Before starting the apps, create a Firebase project, enable the sign-in methods you want to use (Google and Email/Password), and register a web app. Copy `interviewiq/.env.example` to `interviewiq/.env` and fill in the web app configuration values from Firebase. The `.env` file is ignored by Git; do not commit API keys, service-account credentials, or other secrets.

## Run the full project

Clone the repository and enter its directory:

```bash
git clone https://github.com/NandiniPD/Interview-IQ.git
cd Interview-IQ
```

Install the root launcher and each app's dependencies:

```bash
npm install
npm --prefix interviewiq install
npm --prefix aptitude/backend install
npm --prefix aptitude/frontend install
npm --prefix HR/backend install
npm --prefix HR/frontend install
```

Start all three frontends and both backends with one command from the repository root:

```bash
npm start
```

Keep that terminal open while using the apps. Press **Ctrl+C** in it to stop the services.

> If a port is already in use, stop the other app or terminal using it before starting the project.

## Optional AI providers

The InterviewIQ frontend uses Firebase Authentication. The HR interview backend defaults to mock AI mode, so it can run without an AI provider key. To use a supported provider, create `HR/backend/.env` and configure `AI_MODE` (`openai` or `gemini`) and the matching `OPENAI_API_KEY` or `GEMINI_API_KEY`. Keep `.env` files and API keys private.

## Project layout

```text
Interview_Iq/
├── interviewiq/          # Main React + Firebase application
├── aptitude/
│   ├── backend/          # Aptitude Express API (port 5001)
│   └── frontend/         # Aptitude React app (port 3001)
├── HR/
│   ├── backend/          # HR interview Express API (port 5000)
│   └── frontend/         # HR interview React app (port 3002)
├── package.json          # Starts all five services together
└── README.md
```
