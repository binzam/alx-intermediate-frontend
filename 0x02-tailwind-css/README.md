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
- These 3 lines are tailwind directives tht tell Tailwins CSS how to generate the neccessary styles.
  **input.css**

```CSS
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- npx tailwindcss -i ./src/input.css -o ./src/output.css --watch : build our CSS file
  **Note** : To see Tailwind CSS take effect you need to leave this CLI open and running all through out your testing of the project.

**Alternatively** we can use Tailwind CSS via a CDN (Content Delivery Network).

- It allows us to quickly use Tailwind CSS without needing to install or configure it locally.
- This can be done by including a script tag inside the head tag or at the end of the body tag inside the html.

```html
<head>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
```

**or**

```html
<script src="https://cdn.tailwindcss.com"></script>
</body>
```

**Note**: For larger projects or production applications, it's better to set up Tailwind locally and customize it as needed.
