# Messaging App UI

This is the front-end for a full-stack messaging application. Built with React and Vite, it provides a chat interface for user authentication, messaging, and profile management.

**[Live Demo](https://topmessage.netlify.app/)**

**[Backend Repository](https://github.com/sum4n/messaging-app-api)**

---

## Features

- **User Authentication:** Register and login forms with JWT token management.
- **Chat Interface:** View conversations, send messages, and see message history.
- **Profile Management:** Edit your display name.
- **Protected Routes:** Guest and protected route wrappers using React Router.

---

## Technology Stack

- **Runtime Environment:** Node.js
- **Framework:** React 19
- **Build Tool:** Vite
- **Routing:** React Router
- **Styling:** CSS Modules
- **HTTP Client:** Fetch API

---

## Local Development Setup

Ensure you have **Node.js (v18+)** installed.

### 1. Clone & Install

```bash
git clone https://github.com/sum4n/messaging-app-ui.git
cd messaging-app-ui
npm install
```

### 2. Configure Environment Variables

Create a `.env` file in the root directory:

```env
VITE_API_URL=http://localhost:3000
```

This should point to your backend API. For production, set it to your deployed backend URL.

### 3. Run Development Server

```bash
npm run dev
```

### 4. Build for Production

```bash
npm run build
```

### 5. Preview Production Build

```bash
npm run preview
```

---

## What I Learned

- **React State Management:** Managed component state with `useState` and derived values for form validation.
- **Controlled Components:** Built forms with controlled inputs for real-time validation and error handling.
- **Component Composition:** Split complex components into smaller, focused pieces using props.
- **Authentication Flow:** Implemented JWT token storage, protected routes, and logout functionality.
- **Promise Return Values in Async Functions:** Learned how returning values from `.then()` and `.catch()` lets an async function communicate success or failure to its caller. This allowed the profile form to know whether to close after submission or stay open for corrections.
- **Fetch Error Handling:** Managed three distinct error states (validation, server, network) in data fetches.
- **State Reset with `key` Prop:** Used `key` prop to force React to unmount `ChatWindow` when switching conversations, resetting state without manual cleanup.
- **Derived State with `.filter()`:** Computed `emailErrors` and `passwordErrors` from single `validationErrors` array instead of separate states, eliminating sync bugs.
- **Updater Function Pattern:** Used `setState(prev => ...)` to avoid stale state in rapid updates.
- **Conditional Rendering over `hidden`**: Using conditional rendering instead of HTML `hidden` attribute to prevent CSS overrides from breaking UI.
- **Deployment:** Configured Netlify redirects for client-side routing.

---

## Acknowledgments

- Built as a capstone project during [The Odin Project](https://theodinproject.com) Full-Stack JavaScript curriculum.

---
