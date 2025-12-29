[![Open In Colab](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)

# Error Bars in Atomic Scale
Scientific measurement is often associated with uncertainties, so we need accurate accounting for error analysis. Wherever possible these should be indicated on plots and graphs. Showing the error effectively can make plot convey much more complete information. A dedicated Matplotlib method, `errorbar()` allow this, for full documentation see [here](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)

## Prior Data
- Standard Deviation
- Confidence Interval
- Gaussian Process Regression

## Preliminaries 
```python
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt
import numpy as np
```

## Key arguments
```python
errorbar(x, y, yerr, xerr, fmt, ecolor, elinewidth, capsize, capthick)
```
- `x and y`: the array of N data points to be plotted
- `yerr and xerr`: determine the size of the error bars
- `fmt`: controls the format of the data markers and connecting points, as `https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip`
- `ecolor`: sets the color of the error bars
- `elinewidth`: changes the thickness of the error lines
- `capsize`: sets the length of the error bar caps in points (defaults to 0: no error bar caps)
- `capthick`: the thickness the error bar caps.

## Reference:
- [UCD-Physics](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)
- [Jake VanderPlas](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip~:text=In%20visualization%20of%20data%20and,errorbar%20.)
- [Scikit-Learn](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)


# P10.1 Simple Basic Errorbars
A basic errorbar can create with a single Matplotlib function call. The `errorbar` fucntion has many options to fine-tune the outputs. Using these additional options such as `color`, `capsize`, can easily customize the aesthetics of our errorbar plot. 


```python
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt
import numpy as np

# The data is y = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(x) + dy * https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(10)
dy = 0.1
x = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(0, 5, 10)
y = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(x) + dy * https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(10)
xerr = x * 0.1

https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(x, y, yerr=dy, xerr=xerr, fmt='o', color='black', capsize=4)
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("x") 
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("y") 
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("Error bar plot with noise") 
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
```
![](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip%20bar%20svg/Error%20bar%20with%https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)

# P10.2 Continuous Errors in Ohm's Law
All experimental measurements have some degrees of uncertainty, often referred to as an _error_. Here we'll visualize such a continuous error measurement of _Ohm's Law_.

## Description of Ohm's Law
The current that flows through most subtances is directly proportional to the voltage $V$ applied to it. The German Physicist Georg Simon __Ohm__ (1787-1854) was the first to demonstrate experimentally that the current in a metal wire is __directly proportial to the voltage applied__:
<p align="center">
  $I\; \infty\; V$
  
<p align="center">
  $V=IR$
</p>

where $V$ is the voltage measured in volts across the object in question, I is the current measured through the object in amps, and $R$ is the resistance in units of ohms. For full information is [here](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(OpenStax)/University_Physics_II_-_Thermodynamics_Electricity_and_Magnetism_(OpenStax)/09%3A_Current_and_Resistance/9.05%3A_Ohm's_Law)

```python
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt
import numpy as np

#set default font and figure sizes
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip['https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip'] = (6,4)
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip['https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip'] = 12
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip['https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip'] = 'tight'

# Load a Sample data set
# run cell to download data file
V, I_mA, Ierr_mA = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip', unpack=True)

# Basic Errorbars
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(V, I_mA, Ierr_mA, fmt='.k');

https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("Measurements of Ohm's Law")
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("Voltage (V)")
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("Current (mA)")
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Error bar Ohm https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip', bbox_inches='tight')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
```
![](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip%20bar%20svg/Error%20bar%20Ohm%https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)

## Overlay theory and errorbars in both dimensions
Let's assume that the Ohm's Law experiment was conducted with a $1k\Omega$ and that the voltage measurement had an uncertainty of 0.1 V. We can plot errors in both dimensions.

```python
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt
import numpy as np

# Load a Sample dataset
# run cell to download data file
V, I_mA, Ierr_mA = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip', unpack=True)

# convert I_mA to A
I = I_mA * 1e-3
Ierr = Ierr_mA * 1e-3

R = 1_000
I_Theory = V/R

Verr = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(V) * 0.1

# create the errorbars
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(V, I, xerr=Verr, yerr=Ierr, capsize=3, fmt='o', markersize=5, label='Measurements')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(V, I_Theory, label='Theory')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip("Measurements of Ohm's Law")
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Voltage (V)')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Current (A)')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Error bar Ohm Law https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip', bbox_inches='tight')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
```
![](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip%20bar%20svg/Error%20bar%20Ohm%20Law%https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)


# P10.3 Continuous Errors in Gaussian Regression
In this work, we will try a simple Gaussian process regression, using the Scikit-Learn API (for details, see [Introducing Scikit-Learn](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)). This method for fitting a very flexible non-parametric function to data with a continuous measure of the uncertainty. 

## Basics of Gaussian Process regression
Gaussian process regression (GPR) is supervised learning method used to solve regression and probabilistic classification problems. GPR has been applied to solve several different types of real-world problems, including one in materials science, chemistry, physics, and biology.

## Python implementation and Scikit-Learn
The Scikit-Learn version is implemented mainly upon NumPy, which is simple and easy to use, but has limited hyperparameter tuning options.

To illustrate how kernel work in GPR, we will look at a simple dataset curated intentionally. We will start by generating a synthetic dataset. The true generative process is defined.
<p align="center">
  $f(x)\;=\; x\; sin(x)$
</p>

## Key Arguments
```python
from https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip import GaussianProcessRegressor
from https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip import RBF
import numpy as np
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt
```
`GaussianProcessRegressor`: the main class for Gaussian Process regression in scikit-learn.
`RBF`: Radial Basis function kernel (squared exponential kernel)

```python
model = lambda x: x * https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(x)
```
`model`: a simple function 

```python
kernel = RBF(length_scale=1.0)
gp = GaussianProcessRegressor(kernel=kernel, n_restarts_optimizer=10)
```
`kernel`: defines the covariance function of Gaussian process

```python
from https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip import GaussianProcessRegressor
from https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip import RBF
import numpy as np
import https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip as plt

# The model and draw some data
model = lambda x: x * https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(x)
xdata = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip([1, 3, 5, 6, 8, 10, 12])
ydata = model(xdata)

# Define kernel (RBF with initial length scale)
kernel = RBF(length_scale=1.0)

# Compute the Gaussian process fit
gp = GaussianProcessRegressor(kernel=kernel, n_restarts_optimizer=10)

#fit the model
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(xdata[:, https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip], ydata)

xfit = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(start=0, stop=10, num=1000)
yfit, ystd = https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(xfit[:, https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip], return_std=True)

# Visualize the result
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(xdata, ydata, 'or', label=r'$f(x) = x \sin(x)$')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(xfit, yfit, color='gray', label='Gaussian Prediction', linestyle='dotted')

https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(xfit, yfit - 2*ystd, yfit + 2*ystd, color='gray', alpha=0.2, label='Confidence Interval')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip(0, 10)
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('$x$')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('$f(x)$')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Gaussian process regression')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip('Scikit-Learn https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip', bbox_inches='tight')
https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip()
```
![](https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip%20bar%20svg/Scikit-Learn%https://github.com/dindagustiayu/Error-Bars-and-Scikit-Learn-Visualizations/raw/refs/heads/main/error bar svg/Visualizations_Scikit_Learn_and_Error_Bars_v2.1.zip)
