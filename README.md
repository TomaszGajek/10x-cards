# 10x-cards

## Table of Contents
1.  [Project Description](#project-description)
2.  [Tech Stack](#tech-stack)
3.  [Getting Started Locally](#getting-started-locally)
4.  [Available Scripts](#available-scripts)
5.  [Project Scope](#project-scope)
6.  [Project Status](#project-status)
7.  [License](#license)

## 1. Project Description
10x-cards is an application designed to help users quickly create and manage educational flashcard sets. It leverages Large Language Models (LLMs) via an API to generate flashcard suggestions based on user-provided text. The primary goal is to reduce the time and effort required for manual flashcard creation, making the effective learning method of spaced repetition more accessible.

## 2. Tech Stack

### Frontend
*   **Astro 5:** For building fast, content-focused websites with minimal JavaScript.
*   **React 19:** For interactive UI components.
*   **TypeScript 5:** For static typing and improved code quality.
*   **Tailwind CSS 4:** For utility-first CSS styling.
*   **Shadcn/ui:** For a library of accessible React components.

### Backend
*   **Supabase:** A comprehensive backend solution providing:
    *   PostgreSQL database.
    *   Backend-as-a-Service (BaaS) SDK.
    *   Built-in user authentication.

### AI
*   **OpenRouter.ai:** Provides access to a wide range of LLMs (e.g., OpenAI, Anthropic, Google) for generating flashcard content.

### CI/CD & Hosting
*   **GitHub Actions:** For continuous integration and deployment pipelines.
*   **DigitalOcean:** For hosting the application via Docker images.

## 3. Getting Started Locally

### Prerequisites
*   **Node.js:** Version `22.15.0` (as specified in `.nvmrc`). It's recommended to use a Node version manager like nvm.
*   **npm** (or yarn/pnpm)

### Setup
1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd 10x-cards 
    ```
    *(Replace `<repository-url>` with the actual URL of this repository)*

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project and add the necessary environment variables (e.g., Supabase URL, Supabase anon key, OpenRouter API key). Refer to `.env.example` if available (Note: an example file should be created).
    ```env
    # Example .env content
    PUBLIC_SUPABASE_URL=your_supabase_url
    PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
    OPENROUTER_API_KEY=your_openrouter_api_key
    ```

4.  **Run the development server:**
    ```bash
    npm run dev
    ```
    The application should now be running locally, typically at `http://localhost:4321`.

## 4. Available Scripts

The `package.json` file includes the following scripts:

*   `npm run dev`: Starts the Astro development server.
*   `npm run build`: Builds the application for production.
*   `npm run preview`: Previews the production build locally.
*   `npm run astro`: Provides access to the Astro CLI.
*   `npm run lint`: Lints the codebase using ESLint.
*   `npm run lint:fix`: Lints the codebase and attempts to fix issues automatically.
*   `npm run format`: Formats the code using Prettier.

## 5. Project Scope

### Key Features (MVP)
*   **Automatic Flashcard Generation:** Users can paste text, and the application will use an LLM to suggest flashcards (question/answer pairs) for review, editing, or rejection.
*   **Manual Flashcard Management:** Users can manually create, edit, and delete flashcards.
*   **User Authentication:** Basic registration, login, and account deletion functionalities.
*   **Spaced Repetition Integration:** Flashcards are integrated with a pre-existing spaced repetition algorithm for learning sessions.
*   **Data Storage:** User and flashcard data are stored securely and scalably.
*   **Generation Statistics:** Tracking of how many AI-generated flashcards are accepted by users.
*   **Legal Compliance:** User data and flashcards are handled in accordance with GDPR, including the right to access and delete data.

### Out of Scope (for MVP)
*   Advanced, custom-built spaced repetition algorithm.
*   Gamification features.
*   Native mobile applications (current focus is web-only).
*   Importing from multiple document formats (e.g., PDF, DOCX).
*   Publicly accessible API for third-party use.
*   Sharing flashcards between users.
*   Advanced notification system.
*   Advanced keyword search for flashcards.

## 6. Project Status
*   **Current Version:** `0.0.1` (as per `package.json`)
*   The project is currently in the Minimum Viable Product (MVP) development phase. Active development is focused on implementing the core features outlined in the project scope.

## 7. License
This project is currently unlicensed.
