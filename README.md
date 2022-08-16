# Andalusia-Submodules

## The issue

## The NPM Approach

## Why NPM Approach Failed!

## Git Inside Git

## How To Create Submodule

### Submodule Repo

```bash
git submodule add <repo-link> <path>
```

This will craete or update `.gitmodules`

### Submodule From Current Project

```bash
cd <path-to-folder>
git init
git add -N . | git commit -am "create submodule"
git remote add origin <submodule-repo-link>
git push origin master
cd <path-to-superproject>
rm -rf <path-to-folder>
rm -rf .git/modules/<path-to-folder-name>
git submodule add <repo-link> <path>
```

## How To Use Submodule

### Clone The Superproject

```bash
git clone --recurse-submodules <superproject-link>

# or

git clone <superproject-link>
git submodule update --init
```

### Edit Submodlue

```bash
cd <path-to-submodule>
git checkout <target-branch>
git push origin <target-branch>

# or

git submodule foreach 'git status || :'
git submodule foreach git checkout <target-branch>
git submodule foreach git push origin <target-branch>
```

### Update Submodule

```bash
# in superproject

git fetch

# or

git pull origin <target-branch>
```

## Submodule in Action
