# WordFlow

WordFlow is a single-file blogging platform demo built with plain HTML, CSS, and JavaScript. It provides a reading experience, authentication flow, writing editor, user dashboard, comments, profile settings, and an admin panel, all inside one self-contained front-end file with browser storage persistence.

## Preview
[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://nit-blogpost.netlify.app/)

## Overview

The application is structured as a standalone browser app with multiple page sections toggled in the DOM rather than separate routes or backend-rendered screens.  It includes a home feed, post detail view, authentication screen, editor, dashboard, admin area, and a modal for viewing a local users database. 

## Features

- Browse published posts from a home feed with search and category filtering.
- Open individual articles with author information and a comments section.
- Sign in or create an account through a built-in authentication UI. 
- Create, preview, save drafts, publish, edit, and discard posts in the editor. 
- Manage personal posts and account settings from the dashboard. 
- Upload or remove profile avatars and update account details. 
- Access an admin panel for moderation and management tasks. 
- Store users, credentials, posts, comments, and current-session data in `localStorage`. 

## Tech Stack

| Layer | Implementation |
|---|---|
| Markup | HTML document with embedded page sections.  |
| Styling | Embedded CSS using custom properties, responsive layout rules, and reusable UI classes.  |
| Logic | Vanilla JavaScript for state, rendering, auth, editor actions, navigation, and persistence.  |
| Storage | Browser `localStorage` for app data persistence.  |

## Included Demo Data

The source includes mock users, categories, demo credentials, seed posts, and comments so the interface works immediately in a browser without setup.  Demo accounts are provided for `elena@wordflow.com`, `daniel@wordflow.com`, and `priya@wordflow.com`, and the login hint in the app shows the password as `password`. 

## Project Structure

Although the app is contained in one file, it is logically organized into these parts:

- **Theme and layout:** global styles, color tokens, typography, buttons, cards, forms, and responsive layout rules. 
- **Page containers:** home, post detail, auth, editor, dashboard, admin panel, and users database modal. 
- **Mock data:** users, categories, credentials, and starter posts. 
- **State management:** current user, auth mode, editor mode, selected category, search state, and loaded content collections. 
- **Render functions:** functions that update the navbar, feed, article page, auth screen, editor, dashboard, and admin views. 
- **Persistence helpers:** functions that save and reload app data from browser storage.

## Getting Started

1. Save the source as `index.html`. 
2. Open the file directly in a modern browser. 
3. Browse posts as a guest, or sign in with one of the demo accounts. 
4. Create a new post from the dashboard, save it as a draft, or publish it. 

For a simple local development workflow, serving the file through a lightweight static server is also appropriate because the app is front-end only. 


## Demo Login

| Account | Email | Password | Type |
|---|---|---|---|
| Elena | `elena@wordflow.com` | `password`  | `Admin` 
| Daniel | `daniel@wordflow.com` | `password`|  `user`|
| Priya | `priya@wordflow.com` | `password`  |  `user`|

## Main Screens

### Home Feed

The home screen shows the latest posts, a search box, category browsing, and article cards with author and date metadata. 

### Authentication

The auth page supports both sign-in and sign-up modes, validates duplicate emails, and creates new user records in local storage. 

### Editor

The editor supports title, category, featured image URL, excerpt, content writing, preview mode, draft saving, and publishing or updating posts. 

### Dashboard

The dashboard includes tabs for personal posts and account settings, plus actions for creating posts and accessing admin functions when available. 

### Admin Panel

The admin area contains stats, search, moderation actions, and access to the stored users database modal. 

## Data Persistence

This project behaves like a client-side prototype rather than a production full-stack app because it stores data in the browser instead of a backend database.  Users, credential hashes, posts, comments, and active-session details are persisted through `localStorage` helper functions in the script.

## Security Notes

The code explicitly notes that passwords are not stored in plain text, but the hashing shown is a simple browser-side transformation and not production-grade security. The file also states that a real application should use a stronger approach such as bcrypt and a proper backend authentication system.

## Limitations

- No backend API or server-side database is included. 
- Access control is enforced in front-end logic, so it is suitable for demos and learning, not production deployment. 
- Data can be cleared if browser storage is reset.
- The entire app lives in one source file, which makes quick demos easy but long-term maintenance harder. 

## Suggested Repository Layout

```text
wordflow/
├── index.html
└── README.md
```

If this project is expanded, a cleaner structure would separate HTML, CSS, JavaScript, images, and data into dedicated files and folders. [file:1]

## License

No licenseso for this project 
