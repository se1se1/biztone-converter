# GEMINI.md

## Project Overview
**Business Tone Converter (업무 말투 변환기)** is a web-based service designed to convert informal or casual messages into appropriate business language tailored to specific audiences (e.g., bosses, colleagues, clients). It is built as a "One Day Project" for developers to practice AI integration.

### Main Technologies
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla JS).
- **Backend**: Python 3.11+ with **FastAPI**.
- **AI Integration**: **LangChain** and **Upstage Solar-Pro2** LLM.
- **Environment Management**: `python-dotenv` for `.env` files.
- **Deployment**: Vercel (Frontend).

### Architecture
1. **Frontend**: Collects user input and the target audience.
2. **Backend (FastAPI)**: Receives the request, constructs a prompt using templates, and calls the Upstage LLM via LangChain.
3. **AI Engine (Solar-Pro2)**: Generates the converted text.
4. **Backend**: Returns the AI-generated text to the frontend.

---

## Building and Running

### Prerequisites
- Python 3.11 or higher.
- Upstage API Key (configured in `backend/.env`).

### Backend Setup & Execution
1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the FastAPI server:
   ```bash
   uvicorn main:app --reload --port 8000
   ```

### Frontend Execution
1. Open `frontend/index.html` directly in a web browser or use a local development server (like VS Code Live Server).

---

## Development Conventions

### Principles (Vibe Coding Principles)
- **Principle 1: Define Completion Criteria First.** Always refer to the checklist in `PRD_업무말투변환기.md` before starting a task.
- **Principle 2: Research First, Implement Later.** Understand the API or library (e.g., Upstage LangChain integration) before writing code.
- **Principle 3: Analyze Bugs First, Fix Later.** Identify the root cause of an error before applying a fix.
- **Principle 4: Review Before Deployment.** Ensure the full flow (FE -> BE -> AI) is understood.

### Project Structure
- `backend/`: FastAPI application code.
  - `routers/`: API endpoints.
  - `services/`: Core logic including LLM integration.
  - `prompts/`: System prompt templates for different audiences.
  - `models/`: Pydantic schemas for request/response validation.
- `frontend/`: Static web files.
  - `css/`: Stylesheets.
  - `js/`: Client-side logic and API calls.

### Git Guidelines
- Do **not** commit `.env` files. Ensure they are listed in `.gitignore`.
- Follow the structured directory pattern established in the PRD.
