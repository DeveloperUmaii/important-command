📘 React + Vite Project Setup Guide
🚀 Step 1: Create Project

👉 প্রথমে একটা নতুন ফোল্ডার তৈরি করো (যেকোনো নাম দিয়ে)

👉 তারপর terminal open করে নিচের command দাও:

<pre lang="markdown">npm create vite@latest name-of-your-project -- --template react</pre>
📁 Step 2: Enter Project Folder
<pre lang="markdown">cd name-of-your-project</pre>
📦 Step 3: Install Initial Dependencies
<pre lang="markdown">npm install</pre>
🧰 Step 4: Install Main Packages (Dependencies)
<pre lang="markdown">npm install @tanstack/react-query axios daisyui firebase jsonwebtoken lucide-react react-router-dom react-helmet-async react-hook-form react-icons react-simple-captcha react-tabs sweetalert2 swiper tailwindcss recharts react-parallax react-awesome-slider events prop-types</pre>
⚙️ Step 5: Install Dev Dependencies
<pre lang="markdown">npm install -D vite @vitejs/plugin-react eslint postcss autoprefixer globals eslint-plugin-react-hooks eslint-plugin-react-refresh</pre>
🎨 Step 6: Install Tailwind CSS & DaisyUI
<pre lang="markdown">npm install -D tailwindcss@3 postcss autoprefixer daisyui@latest</pre>
🛠️ Step 7: Create Tailwind Config File
<pre lang="markdown">npx tailwindcss init -p</pre>
📄 Step 8: Configure Tailwind

👉 tailwind.config.js ফাইলে নিচের কোড বসাও:

<pre lang="markdown">/** @type {import('tailwindcss').Config} */ export default { content: [ "./index.html", "./src/**/*.{js,ts,jsx,tsx}", ], theme: { extend: {}, }, plugins: [require("daisyui")], } </pre>
🎯 Step 9: Add Tailwind to CSS

👉 src/index.css ফাইলে লিখো:

<pre lang="markdown">@tailwind base; @tailwind components; @tailwind utilities;</pre>
📥 Step 10: Import CSS in main.jsx
<pre lang="markdown">import './index.css';</pre>
🌐 Step 11: Setup Router
🔹 Router File (src/routes/Routes.jsx)
<pre lang="markdown">import { createBrowserRouter } from 'react-router-dom' import LayOut from '../layouts/LayOut' import Home from '../pages/Home' import Login from '../pages/Authentication/Login' const router = createBrowserRouter([ { path: '/', element: &lt;LayOut /&gt;, children: [ { index: true, element: &lt;Home /&gt;, }, { path: '/login', element: &lt;Login /&gt;, }, ], }, ]) export default router; </pre>
⚛️ Step 12: Setup main.jsx
<pre lang="markdown">import React from 'react' import ReactDOM from 'react-dom/client' import './index.css' import { RouterProvider } from 'react-router-dom' import router from './routes/Routes' ReactDOM.createRoot(document.getElementById('root')).render( &lt;React.StrictMode&gt; &lt;RouterProvider router={router} /&gt; &lt;/React.StrictMode&gt; ); </pre>
▶️ Step 13: Run Project
<pre lang="markdown">npm run dev</pre>
🔥 Important Notes

✅ react-router-dom আলাদা করে আবার install করার দরকার নাই (আগেই করা হয়েছে)

❌ নিচেরটা unnecessary:

<pre lang="markdown">npm install react-router-dom</pre>
🧠 Technologies Overview
🌐 Core
react
react-router-dom
🎨 UI & Styling
tailwindcss
daisyui
react-icons
lucide-react
🔄 Data Handling
axios
react-query
📝 Form
react-hook-form
react-simple-captcha
🔐 Auth
firebase
jsonwebtoken
✨ UI Effects
sweetalert2
swiper
recharts
react-tabs
react-parallax
react-awesome-slider
react-helmet-async
🧾 Git Commands
<pre lang="markdown">git init</pre> <pre lang="markdown">git add .</pre> <pre lang="markdown">git commit -m "first commit"</pre> <pre lang="markdown">git branch -M main</pre> <pre lang="markdown">git remote add origin YOUR_REPOSITORY_LINK</pre> <pre lang="markdown">git push -u origin main</pre>
✅ Final Flow Summary (Short)
Create Project
Enter Folder
Install Base
Install Packages
Install Dev Tools
Setup Tailwind
Config Files
Setup Router
Run Project

# All important Command


### Creat Project

<!-- 
<pre lang="markdown">C o m m a n d</pre>
 -->
<pre lang="markdown">npm create vite@latest name-of-your-project -- --template react</pre>
....................,,,,,,,,,,,,,,,,
# Step One
a. Computer adatabase a Ekta new folder toyri kora jekono ba project er nam diye
b. file theke command line a giye command kore project toyri kora
<pre lang="markdown">npm create vite@latest name-of-your-project -- --template react</pre>
c. er cd diye project a giye jaja proyojon install kora 

### 🛠️ **_Technologies & Packages Used_**

---

#### 🌐 **<u>Core & Routing</u>**
* **react**: ইন্টারফেস তৈরির মূল লাইব্রেরি।
* **react-dom**: ব্রাউজারের সাথে রিয়্যাক্টকে কানেক্ট করার মাধ্যম।
* **react-router-dom**: অ্যাপ্লিকেশনে বিভিন্ন *পেজ নেভিগেশন* বা রাউটিং করার জন্য ব্যবহৃত।

#### 🎨 **<u>Styling & UI</u>**
* **tailwindcss**: ইউটিলিটি-ফার্স্ট CSS ফ্রেমওয়ার্ক দ্রুত ডিজাইনের জন্য।
* **daisyui**: টেলউইন্ডের ওপর ভিত্তি করে তৈরি করা কম্পোনেন্ট লাইব্রেরি।
* **autoprefixer** & **postcss**: ব্রাউজার কম্প্যাটিবিলিটি এবং CSS প্রসেসিং নিশ্চিত করে।
* **lucide-react** & **react-icons**: অ্যাপে বিভিন্ন সুন্দর *আইকন* যোগ করার জন্য।

#### 🔄 **<u>Data Fetching & State</u>**
* **axios**: সার্ভার থেকে API-এর মাধ্যমে ডেটা নিয়ে আসার জন্য।
* **@tanstack/react-query**: সার্ভার সাইড ডেটা ম্যানেজমেন্ট এবং *ক্যাশিং* করার জন্য।

#### 📝 **<u>Form & Validation</u>**
* **react-hook-form**: সহজে এবং দ্রুত ফর্ম হ্যান্ডলিং করার জন্য।
* **react-simple-captcha**: সিকিউরিটির জন্য সিস্টেমে *ক্যাপচা* যোগ করতে।

#### 🔐 **<u>Authentication & Security</u>**
* **firebase**: ইউজার লগইন এবং রিয়েল-টাইম ডেটাবেজ ম্যানেজমেন্টের জন্য।
* **jsonwebtoken (JWT)**: ব্যবহারকারীর পরিচয় নিশ্চিত করতে সিকিউর *টোকেন হ্যান্ডলিং*।

#### ✨ **<u>UI Components & Effects</u>**
* **sweetalert2**: ব্যবহারকারীকে সুন্দর পপ-আপ বা *অ্যালার্ট মেসেজ* দেখানোর জন্য।
* **swiper** & **react-awesome-slider**: আকর্ষনীয় স্লাইডার বা ব্যানার তৈরির জন্য।
* **recharts**: ডেটা বা পরিসংখ্যানকে *চার্ট ও গ্রাফের* মাধ্যমে দেখানোর জন্য।
* **react-tabs**: কন্টেন্টগুলোকে বিভিন্ন ট্যাবে ভাগ করে সাজানোর জন্য।
* **react-parallax**: স্ক্রল করার সময় প্রফেশনাল *প্যারালাক্স ইফেক্ট* দেওয়ার জন্য।
* **react-helmet-async**: প্রতিটি পেজের জন্য আলাদা আলাদা টাইটেল এবং *SEO মেটা ট্যাগ* ম্যানেজমেন্ট করতে।

---
## মূল প্যাকেজগুলো (Dependencies):
<pre lang="markdown">npm install @tanstack/react-query axios daisyui firebase jsonwebtoken lucide-react react-router-dom react-helmet-async react-hook-form react-icons react-simple-captcha react-tabs sweetalert2 swiper tailwindcss recharts react-parallax react-awesome-slider events prop-types</pre>
## ডেভেলপমেন্ট টুলস (Dev Dependencies):
<pre lang="markdown">npm install -D vite @vitejs/plugin-react eslint postcss autoprefixer globals eslint-plugin-react-hooks eslint-plugin-react-refresh</pre>


....................,,,,,,,,,,,,,,,,

#### Cd name-of-your-project


### Initial installations required
<pre lang="markdown">npm install -D tailwindcss@3 postcss autoprefixer daisyui@latest</pre>

###  React-Router-Dom রিয়াক্ট রাউটার ডম পরে আলাদাভাবে ইন্সটল করতে হয়
<pre lang="markdown">npm install react-router-dom</pre>


### Config file and Postcss file Create
<pre lang="markdown">npx tailwindcss init -p</pre>


### 📄 tailwind.config.js ফাইলটা এমন হওয়া উচিত
<pre lang="markdown">/** @type {import('tailwindcss').Config} */
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
</pre>

#### main.jsx বা এন্ট্রি জায়গায় CSS ইমপোর্ট  করতে হবে
<pre lang="markdown">import './index.css';</pre>


### main.jsx file
<pre lang="markdown">import React from 'react'
import ReactDOM from 'react-dom/client'
import './index.css'  // ইমপোর্ট না করলে টেল উইন্ড কাজ করবে না ইনডেক্স সিএসএস
import { RouterProvider } from 'react-router-dom'
import router from './routes/Routes' // রাউটারটাকে পুনরায় আবার ইমপোর্ট করতে হবে

ReactDOM.createRoot(document.getElementById('root')).render(
  React.StrictMode >
        RouterProvider router={router} />
  / React.StrictMode >
);</pre>

### index.css or main.css ফাইল
<pre lang="markdown">@tailwind base;
@tailwind components;
@tailwind utilities;</pre>


### Router file 
<pre lang="markdown">import { createBrowserRouter } from 'react-router-dom'
import Main from '../layouts/LayOut'
import Home from '../pages/Home'
import Login from '../pages/Authentication/Login'

const router = createBrowserRouter([
  {
    path: '/',
    element: LayOut />,
    // errorElement: ErrorPage />,
    children: [
      {
        index: true,
        element: Home />,
      },
      {
        path: '/jobs',
        element: Login />,
      },
    ],
  },
])

export default router;</pre>


### Run Project
<pre lang="markdown">npm run dev</pre>


# git-command
<pre lang="markdown">git init
</pre>
<pre lang="markdown">git add .
</pre>
<pre lang="markdown">git commit -m "first commit"</pre>
<pre lang="markdown">git branch -M main
</pre>
<pre lang="markdown">git remote add origin এইখানে  রিপোজিটরীর অরিজিন সেট করো</pre>
<pre lang="markdown">git push -u origin main</pre>
