# python-ast

This is a fork of the `Lib/lib2to3` directory of https://github.com/python/cpython/.

## How the lib2to3 directory was forked

Source: http://stackoverflow.com/questions/24577084/forking-a-sub-directory-of-a-repository-on-github-and-making-it-part-of-my-own-r

Clone cpython:
```
git clone git@github.com:python/cpython.git
cd cpython
```
Rename the master branch to `upstream-master`:
```
git branch -m upstream-master
```
Create a branch, `upstream-lib2to3` with only the commits from `Lib/lib2to3/`:
```
git subtree split --prefix=Lib/lib2to3/ -b upstream-lib2to3
```
Rename the cpython remote to `upstream`:
```
git remote rename origin upstream
```
Add this repo as the origin and push the `upstream-master` branch:
```
git remote add origin https://github.com/banga/python-ast.git
git fetch origin
git push -u origin upstream-skin
```
Create the `master` branch to start contributing changes:
```
git checkout -b master
echo "..." > README
git add README
git commit -m "Add README"
git push -u origin master
```
