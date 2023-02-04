# mkdocs-jupyter-example

https://marcelmaatkamp.github.io/mkdocs-jupyter-example

# clean 
```
$ jupyter nbconvert --clear-output --inplace  $(find . -name '*.ipynb' | grep -v '.ipynb_checkpoints')
```