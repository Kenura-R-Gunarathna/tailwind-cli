# Tailwin CLI #

The simplest and fastest way to get up and running with Tailwind CSS from scratch is with the Tailwind CLI tool. The CLI is also available as a standalone executable if you want to use it without installing Node.js.

run below command to install all the dependances.

```
npm install
```

Here below steps shoild be done if you are not using our project file.
## Step 1 ##

Install tailwindcss via npm, and create your tailwind.config.js file.

```
npm install -D tailwindcss
npx tailwindcss init
```

## Step 2 ##

Add the paths to all of your template files in your tailwind.config.js file.

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

## Step 3 ##

Add the @tailwind directives for each of Tailwind’s layers to your main CSS file. 


eg :- tailwind.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Step 4 ##

inside the package.json file, edit the script value as,

```
"scripts": {
    "dev": "npx tailwindcss -i tailwind.css -o ./src/css/style.css --watch"
}
```

## Step 5 ##

create a src folder and inside it put the below html code.

Make sure your compiled CSS is included in the (your framework might handle this for you), then start using Tailwind’s utility classes to style your content.

```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/main.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

## Step 6 ##

Build the website

```
npm run dev
```

