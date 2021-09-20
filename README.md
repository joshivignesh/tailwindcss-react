# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.


### npx create-react-app tailwindcss-react
============================
npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9

============================
 ### Replace 

 "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",

with


 "start": "craco start",
     "build": "craco build",
     "test": "craco test",
============================
### create craco.config.cs
and add two plugin as below:
// craco.config.js
module.exports = {
    style: {
      postcss: {
        plugins: [
          require('tailwindcss'),
          require('autoprefixer'),
        ],
      },
    },
  }

============================
### Run npx tailwindcss-cli@latest init to create tailwind.config.cs
============================
### Change tailwind.config.js purge as below
   purge: ['./src/**/*.{js,jsx,ts,tsx}', './public/index.html'],
============================
### Replace index.css contents as below
/* ./src/index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;


