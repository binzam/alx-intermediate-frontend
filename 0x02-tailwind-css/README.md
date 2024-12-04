# TAILWINDCSS

## set up and configuration

## **Steps**

- npm init : create a package.json file

- npm install -D tailwindcss : install Tailwind CSS via npm.

- npx tailwindcss init : initialize the Tailwind configuration file(tailwind.config.js).

- Update the content of the **tailwind.config.js** file to match our working directory.

  **tailwind.config.js**

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./src/**/*.{html,js}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

- mkdir src : create a source directory.

- touch src/input.css : create a file named input.css inside src directory and insert the following code inside it.

  **input.css**

```CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- npx tailwindcss -i ./src/input.css -o ./src/output.css --watch : build our CSS file
