# Notion Widgets Web App

## 1. Project Overview
A lightweight web application designed to provide embeddable widgets for Notion pages. The application will host multiple distinct tools accessible via unique URLs.

## 2. Technical Architecture
- **Framework:** React 18 + Vite (Fast, lightweight).
- **Styling:** Tailwind CSS (Utility-first, easy theming).
- **Routing:** React Router (to access widgets like `/clock`, `/timer`, `/player`).
- **Deployment:** Docker (Nginx Alpine image for serving static files).

## 3. Core Features
1.  **Clock Widget (`/clock`):**
    -   Displays current time.
    -   Options: 12/24h format, show/hide seconds, date display.
    -   Themes: Dark/Light/Transparent.

2.  **Pomodoro/Timer Widget (`/timer`):**
    -   Countdown timer for productivity.
    -   Customizable duration.
    -   Visual progress indicator.

3.  **Ambient Player (`/player`):**
    -   Simple audio player for focus sounds (e.g., Rain, White Noise).
    -   Minimal UI to fit small Notion blocks.

## 4. Design Guidelines
-   **Minimalist:** distraction-free interfaces.
-   **Responsive:** Must work well in Notion's varying column widths (iframe resizing).
-   **Dark Mode Support:** Auto-detect or toggleable to match Notion themes.

## 5. Deployment Instructions
-   Standard `Dockerfile` using multi-stage build (Node build -> Nginx serve).
-   `docker-compose.yml` for easy local startup.
