# All important Command


### Creat Project

<!-- 
<pre lang="markdown">C o m m a n d</pre>
 -->
<pre lang="markdown">npm create vite@latest name-of-your-project -- --template react</pre>

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
