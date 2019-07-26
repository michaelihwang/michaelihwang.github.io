## MICHAELIHWANG.COM

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

With it, website was built from the grounds up using React, CSS, and GitHub Pages.

## React
### Version
* [react](https://github.com/facebook/react): 16.8.6

### React Dependencies
* [react-fontawesome](https://github.com/FortAwesome/react-fontawesome): 0.1.4
* [@fontawesome/fontawesome-svg-core](https://github.com/FortAwesome/react-fontawesome): 1.2.19
* [@fontawesome/free-brands-svg-icons](https://github.com/FortAwesome/react-fontawesome): 5.9.0
* [@fontawesome/free-solid-svg-icons](https://github.com/FortAwesome/react-fontawesome): 5.9.0

## Installation

I prefer to use yarn over npm. On the Terminal, run `yarn` to install all dependencies:

`$ yarn`

## Running
To run and test the React App, go to Terminal and run:

`$ yarn start`

This will open your browser and you can now see immediate changes to your React App as you code.

## Deployment
Now that the React App is built, take the following steps to deploy to GitHub Pages:

**1.** Install the `gh-pages` package via yarn. On the Terminal, run:

`$ yarn add gh-pages`

**2.** Go to the root directory of your repository and add the following line of code:

```
{
...
"homepage": "https://michaelihwang.com"
...
}
```
Note: Without the custom domain, it would otherwise be `"homepage": "https://michaelihwang.github.io"`.

**3.** Finally, add the following scripts to the `package.json`:

```
"scripts": {
  "predeploy": "yarn run build",
  "deploy": "gh-pages -b master -d build",
  ...
},
```

**4.** Deploy the website by running `yarn deploy` on the Terminal:

`$ yarn deploy`

Note: This will deploy the build to `master` branch of your repository, my default branch is configured to `dev`. Make sure you have a separate development branch! Otherwise you'll overwrite to master branch and you'll have to `git revert` or `git reset` to previous.

**5.** Go to your repository's Setting and provide your custom domain. In my case, it's michaelihwang.com

**6.** DONE!

## License
MIT License Copyright © 2019 Michael Hwang
