---
title: Git repository for Unity projects
subtitle: README
author: a.whit ([email](mailto:nml@whit.contact))
date: January 2022
documentclass: scrartcl
colorlinks: True
---

This repository contains an empty [Unity](https://en.wikipedia.org/wiki/Unity_(game_engine)) project that has been prepared for use with Git. In recent versions of Unity, Git should mostly work out-of-the-box -- provided that there is an appropriate .gitignore file -- but the documentation is still a bit fragmented.[^1]

[^1]: The main issue to overcome is the problem of dealing with large (binary) files that Unity produces.]

# Procedure for creating this repository

1. Create an empty project via Unity Hub and the Unity Editor.
2. Initialize Git in the project root:
   
   ``git init``
   
3. Initialize Git Large File Storage (LFS):[^2]
   
   ``git lfs install``
   
4. Download the Unity .gitignore file from the [GitHub gitignore template repository](https://github.com/github/gitignore)[^other_versions] into the repository root:
   
   ```
   wget -O .gitignore https://raw.githubusercontent.com/github/gitignore/main/Unity.gitignore
   ```
   
5. Download the .gitattributes file from the [GitHub for Unity project](https://unity.github.com/) into the repository root:
   
   ```
   wget https://raw.githubusercontent.com/github-for-unity/Unity/master/.gitattributes
   ```
   
6. Create this README in the project root directory.
7. Add all files to the repository: ``git add * .gitattributes .gitignore``. Commit.

[^2]: Assumes git [LFS](https://github.com/git-lfs/git-lfs/blob/main/docs/spec.md) is installed. On Ubuntu: ``sudo apt install git-lfs``.
[^other_versions]: Other version of .gitignore and .gitattributes files are available. The versions from GitHub and GitHub for Unity were chosen because they are the closest thing that could be found to official versions.


