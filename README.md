# ✨ TAILWINDCSS WORKSHOP

### Today you are all going to build your very own landing page, using the Tailwind CSS framework!

<hr/>

## 💭 Assignment

- Dream destination

<hr/>

## 📓 Installing Tailwind

1. `npm init -y`
2. `npm install tailwindcss postcss autoprefixer`
3. `npx tailwind init -p`
4. Create a file **_postcss.config.js_** and add:
   ```js
   module.exports = {
     plugins: {
       tailwindcss: {},
       autoprefixer: {},
     },
   };
   ```
5. Create a file **_tailwind.config.js_** and add:

   ```js
   module.exports = {
     purge: [
       // './**/*.html',
       // './**/*.js',
     ],
     darkMode: 'media', // false or 'media' or 'class'
     theme: {
       extend: {},
     },
     variants: {},
     plugins: [],
   };
   ```

6. Create a file **_tailwind.css_** in your styles folder.

   ```js
   @import 'tailwindcss/base';
   @import 'tailwindcss/components';
   @import 'tailwindcss/utilities';
   ```

7. In your **_index.html_** add:

```html
<link href="/tailwind.output.css" rel="stylesheet" />
```

8. In your file **_package.json_** add:

```json
"tailwind": "postcss ./tailwind.css -o ./tailwind.output.css"
```

9. `npm run tailwind`

<hr/>

## 🎩 Purging Tailwind

1. Go to file **_tailwind.config.js_**
2. Uncomment the following code:

```js
  purge: [
		'./**/*.html',
		'./**/*.js',
	],
```

3. `npm run tailwind`

<hr/>

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
