# MediScribe.AI

MediScribe.AI is a medical appointment assistant designed to help patients better understand and act on what happens during a visit. The system records and transcribes patient–physician conversations, extracts key information, and presents a clear summary with follow-up recommendations and next steps.

## Overview

This repository contains the full application stack for MediScribe.AI:

- Frontend: a Next.js web app for recording, streaming audio, and presenting visit summaries
- Backend: an Express + TypeScript server that manages live transcription, AI processing, and integrations
- AI services: Deepgram for live speech-to-text and OpenAI for classification, summarization, and task assistance

## Features

- Live recording of patient–physician conversations
- Real-time audio streaming and transcription
- Medical terminology normalization for patient-friendly explanations
- Visit summary generation
- Follow-up activity suggestions and next steps
- Secure backend APIs for AI workflow orchestration

## Tech Stack

- Frontend: Next.js, React, TypeScript, Tailwind CSS
- Backend: Node.js, Express, TypeScript
- Real-time transcription: Deepgram
- AI processing: OpenAI
- Authentication/integrations: Firebase, Resend
- Containerization: Docker / Docker Compose

## Repository Structure

```text
MedicAI/
├── README.md
├── backend/
│   ├── README.md
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── package.json
│   ├── src/
│   └── .env
├── frontend/
│   ├── README.md
│   ├── package.json
│   └── app/
├── scripts/
└── .git-crypt/
```

## Getting Started

### Prerequisites

Before running the app locally, make sure you have:

- Node.js 18+
- npm
- Docker and Docker Compose
- Access to required environment variables and secrets

### 1) Install dependencies

Frontend:

```bash
cd frontend
npm install
```

Backend:

```bash
cd backend
npm install
```

### 2) Configure environment variables

The backend uses environment variables for services such as Deepgram, OpenAI, Firebase, and email delivery. A sample or encrypted configuration may be present in `backend/.env`, depending on your local setup.

If your environment requires encrypted secrets, follow the instructions in `backend/README.md` before continuing.

### 3) Run the backend

From the `backend` directory:

```bash
docker-compose up -d
```

Or run in the foreground:

```bash
docker-compose up
```

To stop the services:

```bash
docker-compose down
```

For additional backend setup and secret-handling instructions, see `backend/README.md`.

### 4) Run the frontend

From the `frontend` directory:

```bash
npm run dev
```

Then open the local development URL shown by Next.js in your terminal.

## Development Notes

- The frontend is responsible for the user experience and recording interface.
- The backend handles transcription, classification, AI assistance, and service integrations.
- The project is built to support a secure, clinician-facing medical workflow with patient-friendly outputs.

## Additional Documentation

- `backend/README.md` — backend setup, environment unlock steps, and Docker instructions
- `frontend/README.md` — frontend application details and usage notes

## License

This project currently does not declare a repository-wide license in the root README. Please confirm licensing requirements with the project owner before commercial or public reuse.
