# ✨ TAILWINDCSS WORKSHOP

### Today you're all going to build your very own landing page, using the Tailwind CSS framework and a few other tools!

<hr/>

## 💭 Assignment

A travel agency contacts you to create a landing page for [***insert your dream destination here***]. The page needs to be aesthetically pleasing in order to get the attention of potential travelers.

- **In short:** create a landing page for your dream destination!

<hr/>

## 📓 Installing Tailwind

1. `npm init -y`
2. `npm install tailwindcss postcss autoprefixer`
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
     darkMode: 'media', // false or 'media' or 'class'
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

7. Download the landing page template from [Tailwind Starter Kit](https://www.creative-tim.com/learning-lab/tailwind-starter-kit/documentation/download). Rename the html file from landing.html to index.html

8. In your **_index.html_** add:

```html
<link href="./styles/tailwind.output.css" rel="stylesheet" />
```

9. In your file **_package.json_** add the following in your scripts array:

```json
"tailwind": "postcss ./styles/tailwind.css -o ./styles/tailwind.output.css"
```

10. `npm i postcss-cli`

11. `npm run tailwind`

<hr/>

## 💼 Optional but Recommended

1. Install IntelliSense for Visual Studio Code

<hr/>

## 🎩 Purging Tailwind

1. Go to file **_tailwind.config.js_**
2. Add the following code to your purge array:

```js
  purge: [
		'./**/*.html',
		'./**/*.js',
	],
```

3. `npm run tailwind`

<hr/>

## 🚀 Optional Final Touch

1. Integrate the [AOS](https://michalsnik.github.io/aos/) CDN and get things moving!

## 💥 DON'T FORGET TO HAVE FUN

<hr/>

## 🧘🏽‍♀️ Helpful Links

- [Tailwind Cheatsheet](https://nerdcave.com/tailwind-cheat-sheet)
- [Tailwind Docs](https://tailwindcss.com/docs)
- [Pexels](https://www.pexels.com/nl-nl/)

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
