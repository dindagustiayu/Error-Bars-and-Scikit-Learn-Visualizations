[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

# Error Bars in Atomic Scale
Scientific measurement is pften associated with uncertainties, so we need accurate accounting for error analysis. Wherever possible these should be indicated on plots and graphs. Showing the error effectively can make plot convey much more complete information. A dedicated Matplotlib method, `errorbar()` allow this, for full documentation see [here](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.errorbar.html)

## Prior Data
- Standard Deviation
- Confidence Interval

## Preliminaries 
```python
import matplotlib.pyplot as plt
import numpy as np
```

## Key arguments
```python
errorbar(x, y, yerr, xerr, fmt, ecolor, elinewidth, capsize, capthick)
```
- `x and y`: the array of N data points to be plotted
- `yerr and xerr`: determine the size of the error bars
- `fmt`: controls the format of the data markers and connecting points, as `plt.plot`
- `ecolor`: sets the color of the error bars
- `elinewidth`: changes the thickness of the error lines
- `capsize`: sets the length of the error bar caps in points (defaults to 0: no error bar caps)
- `capthick`: the thickness the error bar caps.

## Reference:
- [UCD-Physics](https://github.com/UCD-Physics/Python-HowTos/blob/main/Error_Bars.ipynb)
- [Jake VanderPlas](https://jakevdp.github.io/PythonDataScienceHandbook/04.03-errorbars.html#:~:text=In%20visualization%20of%20data%20and,errorbar%20.)


# P10.1 Simple Basic Errorbars
A basic errorbar can create with a single Matplotlib function call. The `errorbar` fucntion has many options to fine-tune the outputs. Using these additional options such as `color`, `capsize`, can easily customize the aesthetics of our errorbar plot. 


```python
import matplotlib.pyplot as plt
import numpy as np

# The data is y = np.sin(x) + dy * np.random.randn(10)
dy = 0.1
x = np.linspace(0, 5, 10)
y = np.sin(x) + dy * np.random.randn(10)
xerr = x * 0.1

plt.errorbar(x, y, yerr=dy, xerr=xerr, fmt='o', color='black', capsize=4)
plt.xlabel("x") 
plt.ylabel("y") 
plt.title("Error bar plot with noise") 
plt.show()
```
