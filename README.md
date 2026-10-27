# CampusFlow — Student Management System

A responsive, single-page Student Management System built with HTML, CSS, and vanilla JavaScript. The first project file is `index.html`.

## Run locally
1. Download and extract the ZIP.
2. Open `index.html` in Chrome, Edge, Firefox, or another modern browser.
3. No package installation or build step is required.

## Features
- Dashboard with student count, active enrollment, courses, and average attendance
- Create, edit, delete, search, and filter student records
- Attendance overview and low-attendance indicators
- Course overview
- Export student records to CSV
- Browser localStorage persistence
- Responsive desktop and mobile layout
- Design Patterns explanation page

## Design patterns
- **Singleton:** `StudentStore.getInstance()` shares one data store.
- **Factory:** `StudentFactory.create()` creates standardized student objects.
- **Observer:** `EventBus` broadcasts `students:changed` events to refresh the UI.
- **Strategy:** `FilterStrategies` keeps search, status filtering, and course filtering interchangeable.
- **Module pattern:** Store and event bus expose small public APIs while keeping internal state private.
- **MVC-inspired separation:** data, user actions, and rendering are separated into distinct functions/modules.

## Push to GitHub
Open a terminal in the extracted project folder and run:

```bash
git init
git add index.html README.md
git commit -m "Build CampusFlow student management system"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the example remote URL with the URL of your own empty GitHub repository. If GitHub asks you to authenticate, complete its sign-in flow.

## Enable GitHub Pages
1. Push the files to GitHub.
2. Open your repository → **Settings** → **Pages**.
3. Under the build/deployment source, choose **Deploy from a branch**.
4. Select `main` and `/ (root)`, then save.
5. Wait for the published site URL to appear on the Pages settings screen.

## Important limitations
This is a front-end demo and stores records in the current browser's localStorage. Data is not shared across devices or users. Do not use real sensitive student data. A production system should add a backend API, database, authentication, authorization, audit logs, and server-side validation.
