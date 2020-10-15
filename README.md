# Michael's First Personal Website (Deployed July 2020)!
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

For the longest time, I wanted to build and launch my personal website. So I decided to use this past weekend to make it happen. After hours of coding, googling, and several cups of coffee, it's finally up and running! It's been a ton of fun and learned a lot about React, HTML, CSS along the way. To help others do the same, I wrote the following guide so that it may help deploy their own React-based Web App or Website.

* Note: I built this website using `React`, `CSS`, `GitHub`, and `Yarn`.

* Update 1: Refactored code to `TypeScript` March 2020
* Update 2: Added `Google Analytics` October 2020

## React & TypeScript
### Version
* [react](https://github.com/facebook/react): 16.13.1
* [typescript](https://www.typescriptlang.org/): 3.8.3

### Notable Dependencies
* [react-fontawesome](https://github.com/FortAwesome/react-fontawesome): 0.1.4
* [@fontawesome/fontawesome-svg-core](https://github.com/FortAwesome/react-fontawesome): 1.2.19
* [@fontawesome/free-brands-svg-icons](https://github.com/FortAwesome/react-fontawesome): 5.9.0
* [@fontawesome/free-solid-svg-icons](https://github.com/FortAwesome/react-fontawesome): 5.9.0
* axios: 0.19.2
* gh-pages: 2.0.1
* react-ga: 3.1.2

## Preliminaries
### GitHub Pages
Take a look at [GitHub Pages](https://pages.github.com/) to setup your `username.github.io` repository.

*Note: This guide is made for User/Organization site and not Project site. The procedure for Project Site is slightly different.*

### GitHub Branches
I've created and set the default branch as `dev`. This is because **Personal GitHub Pages must be sourced from the `master` branch.** For that reason, there are two branches to this repository: `master` and `dev`.

I do all of my work on the `dev` branch and deploy the updates to `master` (more on that below).

### Yarn
I prefer to use `yarn` over `npm` as my package manager. I used homebrew to install `yarn`. On the Terminal, run:

`$ brew install yarn`

### Create React App
[Create React App](https://facebook.github.io/create-react-app/docs/getting-started) allows for a quick and lightweight setup of your single-page React App. On the Terminal, run:

`$ yarn create react-app username.github.io`

or

`yarn create react-app username.github.io --template typescript`

If you are building in `TypeScript`.

### TypeScript (March 2020 Update)
After getting into `TypeScript`, I decided to refactor my code. To add TypeScript to `Create React App` first install:

`$ yarn add typescript @types/node @types/react @types/react-dom @types/jest`

Then, rename any file to be a TypeScript file (e.g. `src/index.js` to `src/index.tsx`) and restart your development server!

## Google Analytics (October 2020 Update)
I've added Google Analytics to keep tabs on website visits. Metrics are useful!

## Dependency Installation
With `yarn` (or `npm`), you have access to thousands of packages that others have built (Create React App is one of them).

You can add them to your projects with the command `$ yarn add package`. This will not only download the package and add them to the `node_modules` folder, but update the `"dependencies"` list in `package.json`.

Conversely, you may remove them by running `$ yarn remove package`. Accordingly, this will remove the package from your `"dependencies"` list in `package.json`.

If you cloned/forked this repository or need to install all dependencies, simply run:

`$ yarn`

## Running React App
To run and test the React App, go to Terminal and run:

`$ yarn start`

This will open up the default browser and the compiled React App. Changes in the code, once saved to file, is seen immediately on the browser. This is one of the reasons why I love React and Web Development!

## Deployment
When you're ready, take the following steps to deploy to GitHub Pages:

**1.** Install the `gh-pages` package via yarn. On the Terminal, run:

`$ yarn add gh-pages`

**2.** If you have a custom domain, add the following line of code to `package.json` in the project repository:

```
{
...
"homepage": "https://mydomain.com"
...
}
```

*Note: Without the custom domain, add `"homepage": "https://username.github.io"` instead.*

**3.** In addition, add the following scripts to the `package.json`:

```
"scripts": {
  "predeploy": "yarn run build",
  "deploy": "gh-pages -b master -d build",
  ...
},
```

*Note: Notice the script: `"deploy": "gh-pages -b master -d build`. This is pushing the build to the `master` branch. More on that below.*

**4.** Deploy the website by running the following command on the Terminal:

`$ yarn deploy`

*Note: This command will deploy the build to `master` branch of the project repository. Recall that my default branch is configured to the `dev` branch and that I do all of my development work there. **Make sure that you have a separate branch for your source files if building a personal GitHub Page Website.** Otherwise, the command will overwrite the `master` branch's contents with the build of the React App, removing all files pre-deployment. This happened to me and had to use `git reset --hard` to recover the source files. Great learning experience!*

**5.** Go to the project's `Setting` Tab and scroll down to `GitHub Pages` section. Under `Custom domain` input box, provide your custom domain: `mydomain.com`. In my case, it's `michaelihwang.com`.

*Note: Every time you deploy, you have to go back to the Setting Tab and provide your custom domain*

**6.** Finally, create a file called `CNAME` in the project's root repository. It should your custom domain as its content:

```
mydomain.com
www.mydomain.com
```

**7.** DONE! Try going to [michaelihwang.com](michaelihwang.com)!

## Closing Words
I hope that this guide was helpful in getting you started with your own React website and deploying it on GitHub Pages. I intend to improve and add content to my website as I get better at Web Development.

Thanks for reading!

## License
MIT License Copyright © 2020 Michael Hwang
