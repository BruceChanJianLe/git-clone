# Git Clone

This repository demonstrates some useful tips about cloning!

## Partial Clone

```bash
# Clone with entire history but without any blob (files)
git clone --filter=blob:none --no-checkout https://github.com/BruceChanJianLe/docker-nvidia-ubuntu-ros.git
# Clone only the latest commit history (1 commit) without any blob (files)
git clone --filter=blob:none --no-checkout --depth 1 https://github.com/BruceChanJianLe/docker-nvidia-ubuntu-ros.git
```

The above cloned repo will have no files and directories, only a .git directory.
Therefore, the next command is sparse-checkout!

## Sparse Checkout

```bash
# Init sparse checkout
git sparse-checkout init --cone
# Select the files and folder to be checkout (using the above repo as example)
git sparse-checkout add scripts README.md
# Finally checkout to that branch
git checkout master
```

Of course, if you missed out anything, you can always add it.
```bash
git sparse-checkout add docker_build
# To disable git sparse checkout feature
git sparse-checkout disable
```
