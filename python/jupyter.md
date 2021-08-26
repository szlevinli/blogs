# Jupyter Notebook

With Anaconda.

## Extensions

> [jupyter contrib nbextensions](https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html)

```bash
# install
conda install -c conda-forge jupyter_contrib_nbextensions

# install javascript and css files
jupyter contrib nbextension install --user
```

Enable the following options for nbextensions:

- Autopep8
- Hiterland
- Scratchpad
- table_beautifier

## Theme

> [jupyter themes](https://github.com/dunovank/jupyter-themes)

```bash
# install
conda install -c conda-forge jupyterthemes

# update
conda update jupyterthemes

# set themem for dark
jt -t onedork -fs 95 -altp -tfs 11 -nfs 115 -cellw 88% -T
```

Solve the problem of the conflict between the background color of the plot and the dark mode.

create `00_startup.py` file in `~/.ipython/profile_default/startup`

```python
from matplotlib import pyplot as plt

plt.style.use('seaborn-dark')
```

```python
# see more options
print(plt.style.available)

# use
from matplotlib import pyplot as plt
plt.style.use('seaborn-dark')

# mixup theme
plt.style.use(['fivethirtyeight','seaborn-deep'])
```
