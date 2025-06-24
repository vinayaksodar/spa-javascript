# JavaScript SPA Router (No Frameworks)

A simple single-page application (SPA) router built using vanilla JavaScript and Vite. It enables navigation between views without reloading the page.

## Features

* Basic client-side routing using `history.pushState`
* View-based rendering with route mapping
* No external frameworks or libraries

## Project Structure

```
spa-javascript/
├── public/
├── src/
│   ├── main.js
│   └── views/
│       ├── Dashboard.js
│       ├── Posts.js
│       └── Settings.js
├── index.html
├── package.json
```

## How to Run

1. Install dependencies:

```bash
npm install
```

2. Start the dev server:

```bash
npm run dev
```

3. Open `http://localhost:5173` in your browser.

## Usage

Use `<a href="/path" data-link>` for navigation links. Views are simple JavaScript modules that export a function returning HTML content.

Example view (`src/views/Dashboard.js`):

```js
export default () => {
  return `<h1>Dashboard</h1>`;
};
```

## Notes

* Routing is handled manually in `main.js`.
* Works only on a development server or proper static server (not `file://`).

## Reference

This project is based on the approach explained in this video:
Build a Router in Vanilla JavaScript

The video also explains how to handle route parameters (e.g., /posts/2), which is not implemented in this version of the code.

