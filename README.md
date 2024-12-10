# Webpack Template
To intall packages run "npm i" 

To run tests run "npm test"

To build run "npm run build"

To start the project in development mode run "npm run dev"

To deploy run "npm run deploy"

## Deploy
Follow these steps to deploy your project to Github Pages:

0. Make a new branch to deploy from by running the command below. You only need to do this the first time you deploy. The rest of the steps should be done every time you deploy or redeploy your project.

   ```bash
   git branch gh-pages
   
2. Make sure you have all your work committed. You can use ```git status``` to see if there’s anything that needs committing.
3. Run
   
   ```bash
   git checkout gh-pages && git merge main --no-edit
   ```
   to change branch and sync your changes from main so that you’re ready to deploy.
4. Now let’s bundle our application into ```dist``` with your build command, i.e.

   ```bash
   npm run build

5. Now there are a few more commands. Run each of these in order:

   ```bash
   git add dist -f && git commit -m "Deployment commit"
   ```
   ```bash
   git subtree push --prefix dist origin gh-pages
   ```
   ```bash
   git checkout main
   ```
   
6. Recall that the source branch for GitHub Pages is set in your repository’s settings. Get this changed to the ```gh-pages``` branch. That should be everything!
