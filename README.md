## Vardar's website

`source` branch contains `jekyll` format source files. Due to a plugin, it is not possible to use Github Pages' jekyll compiler directly.

`master` branch contains the built site (static output).

So I use `source` branch for source, and `master` branch for the generated output.

`jekyyl` must be installed on local computer to be able to build the site.

## Example workflow

```
git checkout source # switch to source
# do your modification, then commit (git add -A / git commit)
jekyyl build # build the site

git checkout master # switch to master (output) branch
mv _site/* . # move everything from output dir, you may also prefer removing everything (except README.md, .gitignore, .nojekyll) from current directory first
git add -A && git commit # commit output to master

git push origin master # push master
git push origin source # push source
rsync -vzrt --delete * root@vardar.biz.tr:/var/www/ # push to site
```
