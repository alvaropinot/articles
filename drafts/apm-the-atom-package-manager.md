# Option # 1
If you really want to have the list of packages and themes in a repo like this one, you can save those package names in a file and add it to git, so you can install them with `apm`, the atom package manager (just like `npm` 😛 )

Something like:

**my-awesome-packages.txt**
```
linter-eslint
flex-tool-bar
merge-conflicts
seti-icons
local-history
atom-live-server
seti-syntax
```

Later on you can open a terminal and run:

```
apm install --packages-file my-awesome-packages.txt
```
example output:
```
Installing linter-eslint to /Home/<user>/.atom/packages ✓
Installing flex-tool-bar to /Home/<user>/.atom/packages ✓
Installing merge-conflicts to /Home/<user>/.atom/packages ✓
Installing seti-icons to /Home/<user>/.atom/packages ✓
Installing local-history to /Home/<user>/.atom/packages ✓
Installing atom-live-server to /Home/<user>/.atom/packages ✓
Installing seti-syntax to /Home/<user>/.atom/packages ✓
```

# Option # 2
Instead of manually maintaining a list of atom packages, you can use a nice feature of `apm`

First of all, create an atom.io account at https://atom.io/packages.

Then you can search and star any atom package you want, just like at github.com.

After starring some atom packages, you can open a terminal and run the following commands:

## List all the package you had starred
```
apm stars
```
example output:
```
Packages starred by you (6)
├── ⭐  docblockr A helper package for writing documentation (66014 downloads, 692 stars)
├── ⭐  file-icons Assign file extension icons and colours for improved visual grepping (788561 downloads, 2546 stars)
├── ⭐  git-time-machine Visually interact with git commit history for a file (22331 downloads, 246 stars)
├── ⭐  language-vue Syntax highlighting for vue component files (8872 downloads, 26 stars)
├── ⭐  linter-eslint Lint JavaScript on the fly, using ESLint (218982 downloads, 591 stars)
└── ⭐  merge-conflicts Resolve git conflicts within Atom (361047 downloads, 1609 stars)
```


## Install all packages you had starred
**here comes the magic! 🎉  🎈**

```
apm stars --install
```
