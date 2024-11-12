# Useful Resources for Programmers

A collection of valuable notes and resources for programmers

I used to have too many opened tabs in my browser, now I'm sharing my links with the community

| Group | Topics |
|-------------------------------|-----|
| [Python](Python/README.md)  | [Pandas](Python/Pandas/README.md) - [NumPy](Python/NumPy/README.md) - [Matplotlib](Python/Matplotlib/README.md) |
| [Javascript](Javascript/README.md)  |  [Node.js](Javascript/Node/README.md) - [React](Javascript/React/README.md) |
| [SQL](SQL/README.md)  |  |
| [Media](Media/README.md)  | [ImageMagick](Media/ImageMagick/README.md) - [FFMpeg](Media/FFMpeg/README.md) |


## Git

### Branches

List existing branches:

```bash
git branch
```

Option -r causes the remote-tracking branches to be listed, and option -a shows both local and remote branches.

```bash
git branch -r
```

Change branch:

```bash
git switch otherbranch
```

or:

```bash
git checkout otherbranch
```

Create new branch:

```bash
git switch -c newbranch
```

Remember: git clone only brings one branch

Set upstream: https://www.youtube.com/watch?v=wBc0WcyTtOA


### Stash

Puts unstaged changes aside, for example before switching branches

```bash
git stash 
```

To also include unstaged files:

```bash
git stash -u 
```

For more detail: https://www.youtube.com/watch?v=-aPoRU5W8lA


### Merge

Typically from the main branch:

```bash
git merge other-branch
```

Can also be done using the option ```--no-commit``` to perform check before applying changes

git merge and rebase: https://www.youtube.com/watch?v=0chZFIZLR_0


### Reverse commits

Rewinds back 5 commits, keeping changes

```bash
git reset HEAD~5
```

Rewinds back 3 commits, discarding changes

```bash
git reset --hard HEAD~3
```

git reset deletes commits, you can also use the revert command to reverse commits by making new commits that cancel changes.

For more detail: 
https://www.youtube.com/watch?v=zV-XwShNx3o


### Pull requests

https://www.youtube.com/watch?v=jRLGobWwA3Y


## Misc

Free resources for developers https://free-for.dev/#/

Online development environment https://codesandbox.io/

Color Palettes https://colorhunt.co/

HTML Templates https://htmlrev.com/





## Remember

Premature optimization is the root of all evils (unknown author)




Contributions are welcomed

