# InterviewIQ Web App

The main InterviewIQ frontend is a React single-page application with Firebase Authentication. For setup and instructions to launch all project applications together, see the [repository README](../README.md).

## Run this app on its own

From the repository root:

```bash
npm --prefix interviewiq install
npm --prefix interviewiq start
```

The development server opens at [http://localhost:3000](http://localhost:3000).

## Firebase Authentication

1. Create a project in the [Firebase console](https://console.firebase.google.com/).
2. Enable the authentication providers you plan to use, such as Google and Email/Password.
3. Register a Firebase web app.
4. Copy `.env.example` to `.env` in this directory and fill in the web app configuration values.

The `.env` file is ignored by Git. Never commit service-account credentials or other private secrets.

## Build

```bash
npm --prefix interviewiq run build
```
