---
permalink: /create-github-page.html
---
# GitHub Page

## Create a new page
* Create a new github repo from your account
* Go to __Settings__ -> __GitHub Pages__ -> __Source__ -> __master branch__
* Create a new file named `index.md` with the following content:
```
---
permalink: /index.html
---
Hello World
```
* Visit your page `https://<your-git-account>.github.io/<your-repo-name>/<page-name>`

## Special pages
`index.md`: Default page 

`404.md`: Page not found


## References
* [Official github documentation](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site)