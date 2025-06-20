# Personal Website
## Correct workflow for updating the website and maintaining git
- If you don't have the repo locally
  - Clone the repo and enter it
  - Clone the PaperMod under themes/
  ```
  git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
  ```
  - Create sister folder with the public branch with 
  `
    git worktree add ../public.graldij.github.io gh-pages
  `
- If you already have the repo locally, then simply need to pull changes from the remote
  - ```
    cd graldij.github.io
    git pull origin main
    
    cd public.graldij.github.io
    git pull origin gh-pages
    ```
- Modify the src code in the `graldij.github.io` folder, test it with `hugo server -D`.
- When satisfied with the changes, stage, commit and push the changes in `graldij.github.io` as
  ```
    git add change/
    git commit -m "Whatever"
    git push origin main
  ```
- Now we can prepare the version to be published by "compiling" and writing the results in `public.graldij.github.io` with 
  ```
    hugo -d ../public.graldij.github.io
  ```
- Now we can enter `public.graldij.github.io` to stage, commit and push the changes to the `gh-pages` branch of the repo
  ```
    git add .
    git commit -m "New Version of Website"
    git push origin gh-pages
  ```
