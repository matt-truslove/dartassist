# 🎯 Dart Assist App

Welcome to the official management application for the Spoons Darts League! This is a comprehensive, web-based platform for managing all aspects of a local darts league, from player registration and fixture generation to live scoring and tournament brackets.

## ✨ Key Features

-   **League & Player Management**: Admins can create new leagues, add/edit/remove players, and manage the overall status of a league ('Drafting', 'Running', 'Completed').
-   **Automated Fixture Generation**: Automatically generate a full round-robin schedule for any number of players when creating a new league, ensuring everyone plays each other once.
-   **Dynamic Schedule & Results**: View the full season schedule. Authorized users can input leg-by-leg results (best of 3) and record high checkout scores. The system automatically calculates the final score and determines the winner.
-   **Live Leaderboard**: A sortable, real-time leaderboard shows current player standings. It tracks wins, losses, points, leg difference, and rank changes from the previous week.
-   **Dart Scorer**: A full-featured `501` dart scorer for both scheduled league matches and friendly games. It includes a "bull up" feature to decide who starts, a numpad for quick score entry, and tracks player averages.
-   **Knockout Tournaments**: Create single-elimination tournament brackets for 4, 8, 16, or 32 players, including guest players. Features a "Cup Draw" animation to reveal the matchups.
-   **Admin Dashboard**: A protected admin area to manage leagues, control the visibility of game weeks, and analyze fixture integrity to find duplicate or missed matches.
-   **Authentication**: A role-based authentication system allows for 'Admin', 'Player', and 'Guest' access levels, ensuring data integrity.

## 🚀 Tech Stack

-   **Framework**: Next.js (with App Router & Turbopack)
-   **Language**: TypeScript
-   **UI**: React & ShadCN UI Components
-   **Styling**: Tailwind CSS
-   **Database**: Firebase Firestore
-   **Authentication**: Firebase
-   **AI (TTS)**: Google Gemini via Genkit

## ⚙️ Environment Setup

The application is configured to connect to two different Firebase projects: one for development and one for production. This is managed through `.env` files.

-   **.env.local**: Contains the configuration for the **Development** database. When this file is present, the app will use the dev environment.
-   **.env**: Contains the configuration for the **Production** database. This file is used as a fallback when `.env.local` is not present.

### Switching Between Environments

-   **To use the Development database:** Ensure the `.env.local` file exists in the root directory.
-   **To use the Production database:** Rename `.env.local` to `_.env.local` (or delete it) and restart the development server.

## 🏁 Getting Started

1.  **Install Dependencies**:
    ```bash
    npm install
    ```

2.  **Run the Development Server**:
    ```bash
    npm run dev
    ```
    The application will be available at `http://localhost:9002`.

## 📜 Available Scripts

-   `npm run dev`: Starts the Next.js development server with Turbopack.
-   `npm run build`: Creates a production-ready build of the application.
-   `npm run start`: Starts the production server.
-   `npm run lint`: Lints the codebase using Next.js's built-in ESLint configuration.
