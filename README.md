# React 18.3 + Vite (Latest) + Tailwind v4 + Shadcn Setup

This guide provides a streamlined setup for a modern React project using Vite, Tailwind CSS v4, and Shadcn UI components.

---

## 🚀 Installation Steps

### 1️⃣ Initialize React with Vite
```sh
npm create vite@latest . --template react
npm install
```

### 2️⃣ Install React 18.3 (Explicitly)
```sh
npm install react@18.3 react-dom@18.3
```

### 3️⃣ Install Tailwind CSS
```sh
npm install tailwindcss @tailwindcss/vite
```

---

## ⚙️ Configuration

### 📌 Vite Configuration (*vite.config.ts*)
```ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [react(), tailwindcss()],
  resolve: {
    alias: {
      "@": "/src",
    },
  },
});
```

### 📌 Tailwind Configuration (*tailwind.config.js*)
```js
module.exports = {
  content: ["./index.html", "./src/**/*.{js,jsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

### 📌 Global CSS (*index.css*)
```css
@import "tailwindcss";
```

### 📌 Path Aliases (*jsconfig.json*)
```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

---

## 🖌️ Shadcn UI Setup

### 1️⃣ Install Shadcn
```sh
npx shadcn@latest init
```

### 2️⃣ Add Components (Example: Button)
```sh
npx shadcn@latest add button
```

### 3️⃣ Import Components
```js
import { Button } from "@/components/ui/button";
```

---

## ✅ You're all set! 🚀
Run the development server with:
```sh
npm run dev
```

Now you have a modern, efficient, and scalable React + Vite + Tailwind + Shadcn setup ready to go!

