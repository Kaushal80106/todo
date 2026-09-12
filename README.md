# React + Vite + Tailwind CSS Todo App

A lightweight, responsive Todo application built with **React 18**, **Vite**, and **Tailwind CSS**. It uses the **React Context API** for global state management and **Browser LocalStorage** for persistent data storage across browser sessions.

🌐 **Live Demo**: [https://todo-six-ochre.vercel.app/](https://todo-six-ochre.vercel.app/)

---

## ✨ Features

- ➕ **Add Todos**: Quick creation of new tasks.
- ✏️ **Edit Todos**: Inline editing of existing task descriptions.
- ❌ **Delete Todos**: Remove tasks from the list with a single click.
- ✅ **Toggle Completion**: Mark tasks as completed or pending with visual feedback (strikethrough & checkbox).
- 💾 **Local Storage Persistence**: Automatically saves tasks locally so data is maintained across page reloads.
- 🎨 **Responsive UI**: Styled with Tailwind CSS for a modern, dark-themed user interface.

---

## 🛠️ Tech Stack

- **Frontend Framework**: [React 18](https://react.dev/)
- **Build Tool / Bundler**: [Vite](https://vitejs.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **State Management**: React Context API (`createContext`, `useContext`)
- **Linting**: ESLint

---

## 📁 Project Structure

```text
todo/
├── public/
├── src/
│   ├── assets/
│   ├── Components/
│   │   ├── index.js          # Component exports
│   │   ├── TodoForm.jsx      # Input form for creating new todos
│   │   └── TodoItem.jsx      # Individual todo row with edit, toggle, and delete controls
│   ├── Context/
│   │   ├── index.js          # Context exports
│   │   └── TodoContext.js    # React Context and custom `useTodo` hook definition
│   ├── App.css
│   ├── App.jsx               # Main application component & state provider logic
│   ├── index.css             # Tailwind directives & global styles
│   └── main.jsx              # React entry point
├── eslint.config.js
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
└── vite.config.js
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) installed (v16+ recommended) along with `npm`.

### Installation

1. **Clone or navigate to the project directory:**
   ```bash
   cd todo
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

### Running the Application

- **Development Server**:
  ```bash
  npm run dev
  ```
  Open the URL displayed in your terminal (typically `http://localhost:5173`) in your browser.

- **Build for Production**:
  ```bash
  npm run build
  ```

- **Preview Production Build**:
  ```bash
  npm run preview
  ```

- **Linting**:
  ```bash
  npm run lint
  ```

---

## 💡 How It Works

1. **Context API (`src/Context/TodoContext.js`)**:
   Defines the `TodoContext` containing the array of `todos` and functions: `addTodo`, `updateTodo`, `deleteTodo`, and `toggleComplete`.

2. **State & LocalStorage (`src/App.jsx`)**:
   `App.jsx` initializes the state and syncs state updates to browser `localStorage` using React's `useEffect` hooks.

3. **Components**:
   - `TodoForm`: Handles user input and triggers `addTodo`.
   - `TodoItem`: Manages individual item state (read-only vs. editing state) and triggers `updateTodo`, `deleteTodo`, or `toggleComplete`.