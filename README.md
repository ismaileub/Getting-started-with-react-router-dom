# Getting Started with React Router

This guide will walk you through setting up a React application using Vite and integrating React Router for client-side routing.

---

## Prerequisites

Before starting, ensure you have the following installed on your machine:
- [Node.js](https://nodejs.org/) (for `npm` command line tool)
- A code editor like [VS Code](https://code.visualstudio.com/)

---

## Bootstrapping a React App with Vite

Follow these steps to create a new React project using Vite:

1. Open your terminal.
2. Run the following commands:

```bash
npm create vite@latest name-of-your-project --template react 
cd name-of-your-project 
npm install react-router-dom localforage match-sorter sort-by
npm run dev
```

3. After running `npm run dev`, you should see output similar to:

```text
VITE v3.0.7  ready in 175 ms
➜  Local:   http://127.0.0.1:5173/
➜  Network: use --host to expose
```

Open the URL printed in the terminal to view your app in the browser.

---

## Adding a Router

Next, we'll configure a `BrowserRouter` for client-side routing in React.

1. Open the `main.jsx` file located in the `src` directory. This is the entry point for your app.
2. Replace the content of `main.jsx` with the following code:

```jsx
    import React from 'react';
    import ReactDOM from 'react-dom/client';
    import {
      createBrowserRouter,
      RouterProvider,
    } from 'react-router-dom';
    import './index.css';
    
    const router = createBrowserRouter([
      {
        path: '/',
        element: <div>Hello world</div>,
      },
    ]);
    
    ReactDOM.createRoot(document.getElementById('root')).render(
      <React.StrictMode>
        <RouterProvider router={router} />
      </React.StrictMode>
    );

```

3. Save the file and refresh your browser to see the changes. You should see "Hello world" displayed on the screen.

---

## Next Steps

Now that your app is set up with React Router:
- Add additional routes to extend your app.
- Use components and layouts to organize your application structure.
- Explore advanced features like nested routes, loaders, and actions for dynamic behavior.

For more details, check out the official [React Router documentation](https://reactrouter.com/).
