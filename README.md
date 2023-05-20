


## Install 
- VSCode editor
- live server extensions for VSCode
- Nodejs 

# Basic Setup steps for tailwind as per documentation:
1.  Initialize the package: To start, create a new directory for your package and run the `npm init` command to initialize the package. This will create a `package.json` file in the directory which holds metadata about the package.
2.  #### Install Tailwind CSS: 
	 Install `tailwindcss` via npm, and create your `tailwind.config.js`  file using following commands.
	 `npm install -D tailwindcss`
`npx tailwindcss init`
3. #### Configure your template paths

	Add the paths to all of your template files in your  `tailwind.config.js`  file.
	`/** @type  {import('tailwindcss').Config} */`
	 `module.exports  =  { '
	 'content: ["./src/**/*.{html,js}"],`
		  `theme:  { extend:  {}, },` 
		  `plugins:  [], `
	  `}`
    
4.  #### Add the Tailwind directives to your CSS

	Add the  `@tailwind`  directives for each of Tailwind’s layers to your main CSS file.
	`src/input.css`
	`@tailwind base;`
	`@tailwind components;`
	`@tailwind utilities;`
    
5.  #### Start the Tailwind CLI build process

	Run the CLI tool to scan your template files for classes and build your CSS.
`npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch`

6. #### Start using Tailwind in your HTML

	Add your compiled CSS file to the  `<head>`  and start using Tailwind’s utility classes to style your content.
 ` src/index.html`

	`<!doctype  html>`
`<html>`
`<head>`
`<meta  charset="UTF-8">`
`<meta  name="viewport"  content="width=device-width, initial-scale=1.0">`
`<link  href="/dist/output.css"  rel="stylesheet">`
`</head>`
`<body>`
`<h1  class="text-3xl font-bold underline text-red-500">`
`Hello world!!!!`
`</h1>`
`</body>`
`</html>`



