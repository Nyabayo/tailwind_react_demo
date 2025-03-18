# How to Set Up and Test Tailwind CSS in a React App

## 1️⃣ Create a New React Project

Run the following command to create a new React project using Vite:

```sh
npx create-vite@latest my-tailwind-app --template react
cd my-tailwind-app
npm install
```

---

## 2️⃣ Install Tailwind CSS, PostCSS, and Autoprefixer

Run the command:

```sh
npm install -D tailwindcss postcss autoprefixer
```

Then, initialize Tailwind:

```sh
npx tailwindcss init -p
```

This creates two configuration files:

- `tailwind.config.js`
- `postcss.config.js`

---

## 3️⃣ Configure Tailwind

Open `tailwind.config.js` and update the `content` section:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

---

## 4️⃣ Add Tailwind Directives

Open `src/index.css` and add the following lines at the top:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 5️⃣ Test Tailwind CSS

Modify `src/App.jsx` to include Tailwind classes:

```jsx
export default function App() {
  return (
    <div className="h-screen flex justify-center items-center bg-gray-900">
      <h1 className="text-4xl font-bold text-white underline">
        Tailwind is working!
      </h1>
    </div>
  );
}
```

---

## 6️⃣ Start the Development Server

Run the following command:

```sh
npm run dev
```

Then open [http://localhost:5173](http://localhost:5173) in your browser to check if Tailwind is working.

For more details, visit: [Tailwind Docs](https://tailwindcss.com/docs/installation/framework-guides)

---

## 7️⃣ Verify Tailwind is Working

If Tailwind is applied correctly, you should see a dark gray background and white text. If it's not working:

- Ensure you added Tailwind directives in `index.css`.
- Restart the dev server: `ctrl + c`, then `npm run dev`.
- Verify `tailwind.config.js` includes the correct `content` paths.

###

---

Now you’re ready to use Tailwind CSS in your React project! 🚀

