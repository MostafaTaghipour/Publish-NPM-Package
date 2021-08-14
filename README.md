
# Create and Publish NPM Packages
In this tutorial, we will show you step by step how to create a package and distribute it through npm.
  

### Choose a package name
Before creating a new repository, it’s worth checking that your package name is available on [npmjs.com](http://npmjs.com/).

### Initialise your project
Create a directory and run npm init:
```bash
mkdir your-package-name
cd your-package-name
npm init
```

The script will ask for different information (such as library name, author name, version etc.)
Then open your package.json
and add required info (name, version, description, keywords, homepage, bugs, rewpository, license)

```json
{
	"name": "my-npm-package",
	"version": "1.0.0",
	"description": "An example package for a tutorial.",
	"keywords": [
		"example",
		"package",
		"tutorial"
	],
	"main": "index.js",
	"scripts": {
		"test": "mocha"
	},
	"homepage": "https://github.com/UserName/package-name",
	"bugs": {
		"url": "https://github.com/UserName/package-name/issues",
		"email": "your-public-email@example.com"
	},
	"repository": {
		"type": "git",
		"url": "https://github.com/UserName/package-name.git"
	},
	"author": "Joe Bloggs <your-public-email@example.com> (your-website.com)",
	"license": "MIT",
	"private": false,
}
```

  
### Initialise Git
Create a new repository, grab the URL and navigate to your project in the terminal. Then type the following:
```bash
git init
git commit -m "first commit"
git branch -M main
git remote add origin {your_github_repository_url}
git push -u origin main
```
  
### Write your codes
Write your code, complete your files and package, and publish it when your package is ready to be released.

### Write a great README
If you’re putting some code into the public domain, you’ll need to explain how other people can use it. Depending on the type and complexity of your project, writing a great README could take up a big proportion of your overall development time!

Thankfully, there are some useful templates out there to get you started more quickly. Here’s  [a link to one of the most popular](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).

I recommend taking a look at popular npm packages with similar functionality to yours, and seeing how they structure their  `README.md`  files. You can also check out  [the 12 most popular packages on the npm homepage](https://www.npmjs.com/).

For a simple product, the bare-minimum  `REAME.md`  file should probably include the following sections:

-   **Installation / Getting Started:**  steps for installing the package and importing it into your app.
-   **Example Code / Quick Start:** a simple example of your package in-action. For a simple package, many people will prefer to see a working example so they can get started straight away — so put this near the top.
-   **Contact Us / Author(s):** some way to know who built the package and how to get in contact with them, should someone want to ask a question, report a bug or contribute to the package. If you’re more serious about getting contributions, you can include a  `CONTRIBUTING.md`file: here’s  [a popular template for that](https://www.contributor-covenant.org/version/1/4/code-of-conduct.html).
-   **License:**  finally, it’s good practice to spell out your license. Again, if you’re more serious, you can create a separate  `LICENSE.md`  file. GitHub has  [a useful guide to licensing, as well as some template files](https://help.github.com/en/articles/licensing-a-repository).

### Add badges
You might be wondering how to get your hands on some of the fancy badges that many of the most popular packages have.
One of the simplest ways to add these to your  `README.md`  file is using  [Shields.io](https://shields.io/).

All you need to do it provide URLs to various services you use, such as your GitHub repo or your package’s page, and Shields.io will give you markdown containing a badge.

### Publish your package
If you’re happy your package is working correctly and you have a good  `README.md`  file, then you’re ready to go live!

-   If you haven’t already,  [sign-up to npm](http://If you haven't already, sign-up to npm.). A profile picture and GitHub link can make you seem more personable if you’re hoping for contributors!
-   Go into your terminal, type  `npm login`  and insert your details.
-   In the terminal, navigate to the root directory of your package run  `npm publish` or if you want to publish your package on a specific npm server run   `npm publish --registry {your_specific_npm_server_url}`
 
### Update your package
Pushing code to your version control system won’t automatically update your npm package. For that, you need to run  `npm publish`  in the terminal.

You cannot override a version or your package that has already been published, so before running  `npm publish`  you should update your app’s version.