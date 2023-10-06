# Deploy React App in Github


**Step 1 :** *To initialize your git repo*
```
git init
```

**Step 2 :** *To add your files in local repo*
```
git add .
```
**Step 3 :** *To commit your changes in the files*
```
git commit -m "[some message]"
```
**Step 4 :** *To add the remote repo url to your local repo*
```
git remote add origin "[repo-url]"
```
**Step 5 :** *This step is optional if you have token for your account, you can add this command*
```
git remote set-url origin "https://[token-key]@github.com/[user-name]/[repo-name]"
```
**Step 6 :**
```
git push origin [branch-name]
```
---
\
**"Till this step is enough for only you're pushing your code into github"**


\
If you're depolying your project follow below steps

\
**Step 7 :** *To install gh-pages dependency in your project*
```
npm install gh-pages --save-dev
```
**Step 8 :** *To add some lines of code to your package.json file in top of the name,version*
```
"homepage": "https://[user-name].github.io/[repo-name]",
```
**Step 9 :** *Again, you add this lines of code to your package.json file inside of script in top of the start,build*
```
"predeploy":"npm run build",  
"deploy":"gh-pages -d build",
```
**Step 10 :** *Final step is to deploy your project in github*
```
npm run deploy
```