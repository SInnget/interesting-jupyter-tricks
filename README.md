# interesting-jupyter-tricks
* collect some interesting jupyter notebook tricks, say magics, widgets, and version control

### Widgets
- interact widget
  https://blog.dominodatalab.com/interactive-dashboards-in-jupyter/

### Magics
https://towardsdatascience.com/jupyter-notebook-hints-1f26b08429ad


##### autoreload

- use autoreload, and import .py package to effectively write code in vs code and run in notebook
https://blog.godatadriven.com/write-less-terrible-notebook-code

- https://ipython.org/ipython-doc/3/config/extensions/autoreload.html
- usage:
```
%load_ext autoreload;
autoreload 2
```
##### writefile
- usage:
```
%%writefile pythoncode.py
import numpy
def append_if_not_exists(arr, x):
    if x not in arr:
        arr.append(x)

def some_useless_slow_function():
    arr = list()
    for i in range(10000):
        x = numpy.random.randint(0, 10000)
        append_if_not_exists(arr, x)
```
### Version controls in jupyter notebook
- save a copy of the notebook in both Python script and HTML format whenever the notebook is saved
https://towardsdatascience.com/version-control-for-jupyter-notebook-3e6cef13392d
