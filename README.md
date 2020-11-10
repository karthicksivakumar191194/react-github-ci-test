# React GitHub CI

## #1 Deploy to GH Pages

> npm install gh-pages --save-dev

Add below snippet in package.json
```json
     "homepage": "https://karthicksivakumar191194.github.io/react-github-ci-test",
      "scripts": {
    	......
    	"predeploy": "npm run build",
    	"deploy": "gh-pages -d build"
    },
```
- **homepage** - URL where the react will be running. This is not related to gh-pages, since we adding the react to sub-directory we adding this to tell create-react-app so production build points to right path.
- We adding two new scripts to react - **predeploy** & **deploy**.
	- **predeploy** - Take build of the project, we will be hosting only the build files.
	- **deploy** - Deploys to the server, we can view the site on github page or custom domain URL as we set. **-d build** refers the destination folder we need to deploy to server. When we run this cmd first time it will create a branch 'gh-pages' in github.

Source Branch for the GitHub Pages needs to set in https://github.com/karthicksivakumar191194/react-github-ci-test/settings


#### Manuall Deploy
When you run **npm run deploy** in terminal, the **npm run build** cmd will run and the folders inside the 'build' pushed to github repo 'gh-pages' branch and you can view the output in the URL 
