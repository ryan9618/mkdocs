## Linux常用软件
### tages:
     - linux
     - Soft


## Mkdocs部署
```
mamba env list
mamba create -n mkdocs-app python=3.8 -y
mamba activate mkdocs-app


pip install  mkdocs
pip install  mkdocs-material

mkdocs build
mkdocs  gh-deploy
```