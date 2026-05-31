# Autodeploy website hosted on GitHub (free)

1.  Create a PUBLIC repository on your GitHub. The PROJECT NAME will be part of the URL (choose accordingly).
2.  In your new repository on GitHub, go to "Settings", "Pages" and select “GitHub Actions”
    ![GitHub Actions](github-actions.png)
3.  Download [the tuto repository](https://github.com/gwenaellegustin/vite-autodeploy-example) and unzip (OR `git clone` and delete .git folder)
4.  Locally, edit package.json and replace "vite-autodeploy-example" with the PROJECT NAME.
    ![package.json](packagejson.png)
5.  Locally in the project folder, do the following commands (do one by one if you have error)
    ```
    git init
    git add .
    git commit -m "init commit"
    git branch -M main
    ```
    In the next command, replace [URL] with your project URL. Example: "https://github.com/gwenaellegustin/test.git"
    ```
    git remote add origin [URL]
    git push -u origin main
    ```
6.  On GitHub, go to Actions and check the green check icon.
    ![Success deployment](deploy.png)
7.  Go to your website: https://[ACCOUNT-NAME].github.io/[PROJECT-NAME]/
    - Example: https://gwenaellegustin.github.io/vite-autodeploy-example/

# Test locally

- First time (installation): `npm i`
- Run website: `npm run dev`

# Edit

- **readme.md**: replace information with your project info
- **Code**: the content (body) of index.html is edited by JS in main.js
- **Assets**: public folder is for directly accessible files (favicon). Other assets can be put in src/assets.
- **Libraries**: to add an another library, run command `npm install --save ...`. (Example with three.js `npm install --save three`)
