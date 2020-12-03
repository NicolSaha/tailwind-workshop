# ✨ TAILWINDCSS WORKSHOP

### Today you're all going to build your very own landing page, using the Tailwind CSS framework and a few other tools!

<hr/>

## 💭 Assignment

A travel agency contacts you to create a landing page for [***insert your dream destination here***]. The page needs to be aesthetically pleasing in order to get the attention of potential travelers.

- **In short:** create a landing page for your dream destination!

<hr/>

## 🐙 Github

1. Create a repository named `tailwind-intro`
2. Be sure to have a README.md file, so that you can link to your final live version on Netlify.
3. Clone it to your laptop.
4. Create a styles folder

<hr/>

## 📓 Installing Tailwind

1. `npm init -y`
2. `npm install tailwindcss postcss-cli postcss autoprefixer`
3. `npx tailwind init -p`
4. Make sure you now have a file **_postcss.config.js_** with:
   ```js
   module.exports = {
     plugins: {
       tailwindcss: {},
       autoprefixer: {},
     },
   };
   ```
5. Make sure you now have a file **_tailwind.config.js_** with:

   ```js
   module.exports = {
     purge: [],
     darkMode: false,
     theme: {
       extend: {},
     },
     variants: {},
     plugins: [],
   };
   ```

6. Create a file **_tailwind.css_** in your **styles folder**.

   ```js
   @import 'tailwindcss/base';
   @import 'tailwindcss/components';
   @import 'tailwindcss/utilities';
   ```

7. Download the landing page template from [Tailwind Starter Kit](https://www.creative-tim.com/learning-lab/tailwind-starter-kit/documentation/download). Rename the html file from **_landing.html_** to **_index.html_**. Don't forget to copy the folder **assets** also into your repository.

8. In your **_index.html_** add:

```html
<link href="./styles/tailwind.output.css" rel="stylesheet" />
```

9. In your file **_package.json_** add the following in your **scripts** array:

```json
"tailwind": "postcss ./styles/tailwind.css -o ./styles/tailwind.output.css"
```

10. `npm run tailwind`

<hr/>

## 💼 Optional but Recommended

1. Install [IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss) for Visual Studio Code

<hr/>

## 🎨 Optional but fun: Colors

All the [tailwind colors](https://tailwindcss.com/docs/customizing-colors#color-palette-reference) available to you. There are some that are extra and not available to you straight away.

You can gain access to them by adding the following code to your file **_tailwind.config.js_**:

```js
const colors = require('tailwindcss/colors');

module.exports = {
  theme: {
    colors: {
      // Build your palette here
      emerald: colors.emerald,
      yellow: colors.amber,
    },
  },
};
```

- The emerald and yellow are just aliases for the colors, and this is how you will access them in your htlm. So yellow text will be: `text-yellow`.

- Adding custom colors to the default tailwind colors is as easy as:

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        'regal-blue': '#243c5a',
        'indigo-lighter': '#b3bcf5',
        'indigo-dark': '#202e78',
      },
    },
  },
};
```

- If the code confuses you a handy tool is [Tailwind Colors](https://tailwind-colors.meidev.co/).

<hr/>

## 🌟 Creating Your Own Components

When you decide that you are happy with your design, you can start extracting your own components from it so that you don't have to re-type the same code in different places.

You will have to create a class for the element you are styling and put all the tailwind classes into an @apply directive.

- A practical example:

```html
<button class="btn-indigo">Click me</button>

<style>
  .btn-indigo {
    @apply py-2 px-4 bg-indigo-500 text-white font-semibold rounded-lg shadow-md hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-400 focus:ring-opacity-75;
  }
</style>
```

- But... instead of putting it in our css we are going to inject it into our file **_tailwind.css_**, which will then look like this:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer components {
  .btn-blue {
    @apply py-2 px-4 bg-blue-500 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75;
  }
}
```

- By doing this Tailwind will automatically move those styles to the same place as @tailwind components, so you don't have to worry about getting the order right in your source files.
You can extract as many components as you want!
<hr />

## 🎩 Purging Tailwind

1. Go to file **_tailwind.config.js_**

2. Add the following code to your **purge array**:

```js

 './**/*.html', './**/*.js',

```

3. `npm run tailwind`

<hr/>

## 🚀 (Really) Optional Final Touch

- Integrate the [AOS](https://michalsnik.github.io/aos/) CDN and get things moving!
- I will make things easy for you and give you the CDN links to add.

1. CSS:

```html
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />
```

2. JS:

```js
<script src='https://unpkg.com/aos@2.3.1/dist/aos.js'></script>
```

3. Create an **_index.js_** file and add the following code to initialize:

```js
<script>AOS.init();</script>
```

- Upload it to [Netlify](https://www.netlify.com/), so that others can see your creation!
- Don't forget to add a file **_.gitignore_** with the following code `node_modules` before you push to github and upload!

## 💥 DON'T FORGET TO HAVE FUN

<hr/>

## 🧘🏽‍♀️ Helpful Links

- [Tailwind Cheatsheet](https://nerdcave.com/tailwind-cheat-sheet)
- [Tailwind Docs](https://tailwindcss.com/docs)
- [Pexels](https://www.pexels.com/nl-nl/)
- [Tailwind Colors](https://tailwind-colors.meidev.co/)
- [Tailwind Color Generator](https://tailwindcolorgenerator.com/)
- [Tailwind Ink](https://tailwind.ink/)

<hr/>

## 🛠 Tools

- [Visual Studio Code](https://code.visualstudio.com/)
- [Markdown](https://www.markdownguide.org/)
- [Tailwind](https://tailwindcss.com/)
- [IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
- [Tailwind Starter Kit](https://www.creative-tim.com/learning-lab/tailwind-starter-kit/presentation)
- [AOS](https://michalsnik.github.io/aos/)
- [Netlify](https://www.netlify.com/)

<hr/>

### 👩🏻‍💻 License

This project is [MIT](https://github.com/NicolSaha/tailwind-workshop/blob/main/README.md) licensed <br/>
© 2020 [Nicol Saha](https://github.com/NicolSaha)
