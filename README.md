# Git Clone

This repository demonstrates some useful tips about cloning!

## Partial Clone

```bash
# Clone with entire history but without any blob (files)
git clone --filter=blob:none --no-checkout https://github.com/BruceChanJianLe/docker-nvidia-ubuntu-ros.git
# Clone only the latest commit history (1 commit) without any blob (files)
git clone --filter=blob:none --no-checkout --depth 1 https://github.com/BruceChanJianLe/docker-nvidia-ubuntu-ros.git
```
