🧭 Custom React Router (Without React Router Library)

A simple React project that demonstrates how to build your own custom page navigation system — similar to React Router — using only React state and conditional rendering.

This project switches between different pages (Page1, Page2, Page3) without reloading the browser and without using any routing libraries.

🚀 Features

🧩 Custom page routing using useState

⚡ Instant navigation without full page reloads

🖱️ Button-based page switching

💡 Acts like a simplified version of React Router

📄 Clean and minimal React codebase

🏗️ Project Structure
📁 src/
 ┣ 📁 components/
 ┃ ┣ 📄 Page1.jsx
 ┃ ┣ 📄 Page2.jsx
 ┃ ┗ 📄 Page3.jsx
 ┣ 📄 App.jsx
 ┣ 📄 App.css
 ┗ 📄 main.jsx

💻 How It Works

The app stores a list of pages in an array and dynamically renders the selected component based on the current state.

const pages = [
  { id: 1, body: <Page1 /> },
  { id: 2, body: <Page2 /> },
  { id: 3, body: <Page3 /> },
];

const [currentPage, setCurrentPage] = useState(0);

return (
  <>
    <button onClick={() => setCurrentPage(0)}>Page 1</button>
    <button onClick={() => setCurrentPage(1)}>Page 2</button>
    <button onClick={() => setCurrentPage(2)}>Page 3</button>

    {pages[currentPage].body}
  </>
);


🧠 This logic mimics the way routing works:

Instead of URL changes, you store the current page index in state.

Clicking a button updates the state (setCurrentPage), and React re-renders that page.

The transition happens instantly without refreshing the entire page.

🛠️ Technologies Used

React.js (Vite Setup)

JavaScript (ES6+)

CSS3 for basic styling

⚙️ Setup and Run

Clone the repository

git clone https://github.com/your-username/custom-react-router.git
cd custom-react-router


Install dependencies

npm install


Run the app

npm run dev


Open the link shown in the terminal (usually http://localhost:5173)

🧩 Future Enhancements

Add URL-based routing with window.history.pushState()

Add a “Back” and “Forward” button functionality

Highlight the active page button

Animate page transitions

Convert into a reusable <CustomRouter> component
