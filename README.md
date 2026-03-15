# Browser Media Downloader (Java + Extension)

A full-stack desktop application and browser extension duo that allows users to download media (videos, images) directly from their web browser to their local machine.

## 🏗️ Architecture

This project is built using a decoupled architecture, separating the browser UI from the local file system operations:

1. **Browser Extension (Frontend):** Injects a UI into webpages or utilizes a context menu to capture media URLs.
2. **Local HTTP Server (Middleware):** A lightweight Java HTTP server running locally (e.g., `localhost:5000`) that listens for download requests from the extension.
3. **Download Engine (Backend):** A Java-based engine utilizing the Factory Pattern to route URLs to the appropriate downloader (e.g., standard HTTP clients for images, `yt-dlp` for complex video streams).
4. **Desktop GUI (Manager):** A JavaFX user interface to monitor active downloads and track progress.

## 🛠️ Tech Stack

* **Language:** Java (JDK 17+)
* **UI Framework:** JavaFX
* **External Tools:** `yt-dlp` (for video stream extraction)
* **Browser Extension:** Manifest V3 (HTML/CSS/JavaScript)

## 🚀 Roadmap (Separation of Concerns)

- [ ] **Phase 1:** Build the core Java Download Engine (`yt-dlp` wrapper via `ProcessBuilder`).
- [ ] **Phase 2:** Implement the Observer Design Pattern for real-time progress tracking.
- [ ] **Phase 3:** Build the lightweight Local HTTP Server in Java.
- [ ] **Phase 4:** Develop the Manifest V3 Browser Extension (Context Menu/Injected Buttons).
- [ ] **Phase 5:** Build the JavaFX Graphical User Interface.
- [ ] **Phase 6:** Integrate components and handle multithreaded downloads.

## 💻 Setup & Installation

*(To be updated as the project progresses)*