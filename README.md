#### All important Command


##Creat Project
<pre lang="markdown"> ```npm create vite@latest name-of-your-project -- --template react``` </pre>
#Cd name-of-your-project


##Initial installations required
<pre lang="markdown"> ```npm install -D tailwindcss@3 postcss autoprefixer daisyui@latest``` </pre>


##Config file and Postcss file Creat
<pre lang="markdown"> ```npx tailwindcss init -p``` </pre>


##📄 tailwind.config.js ফাইলটা এমন হওয়া উচিত
<pre lang="markdown"> ```/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [require("daisyui")], // DaisyUI প্লাগইন যুক্ত
}
``` </pre>


##index.css or main.css ফাইল
<pre lang="markdown"> ```@tailwind base;
@tailwind components;
@tailwind utilities;``` </pre>


##Run Project
<pre lang="markdown"> ```npm run dev``` </pre>