# React 18.3 + Vite latest + Tailwind v4 + Shadcn setup

# React and Tailwind Installation -
npm create vite@latest . --template react
npm install
npm install react@18.3 react-dom@18.3
npm install tailwindcss @tailwindcss/vite

# Tailwind Configuration
*vite.config.ts*
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [react(), tailwindcss()],
  resolve: {
    alias: {
      "@": "/src",
    },
  },
});


*tailwind.config.js*
// eslint-disable-next-line no-undef
module.exports = {
    content: ["./index.html", "./src/**/*.{js,jsx}"],
    theme: {
      extend: {},
    },
    plugins: [],
  };
  
*index.css*
@import "tailwindcss";

*jsconfig.json*
{
    "compilerOptions": {
      "baseUrl": ".",
      "paths": {
        "@/*": ["./src/*"]
      }
    }
  }

# Shadcn installation
npx shadcn@latest init
npx shadcn@latest add button

component import -> import { Button } from "@/components/ui/button";