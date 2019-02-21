### [BaseDistribution](BaseDistribution.md).plot_dist (method)


```py

def plot_dist(self, x, unit=None, label=None, show=False, **kwargs)

```



Plot the analytic distribution function.  Requires matplotlib to be installed.

See also:

* [BaseDistribution.plot](BaseDistribution.plot.md)
* [BaseDistribution.plot_sample](BaseDistribution.plot_sample.md)
* [BaseDistribution.plot_gaussian](BaseDistribution.plot_gaussian.md)

Arguments
-----------
* `x` (np array): the numpy array at which to sample the value on the
    x-axis.
* `unit` (astropy.unit, optional, default=None): units to use along
    the x-axis.  Astropy must be installed.
* `label` (string, optional, default=None): override the label on the
    x-axis.  If not provided or None, will use [BaseDistribution.label](BaseDistribution.label.md).  Will
    only be used if `show=True`.
* `show` (bool, optional, default=True): whether to show the resulting
    matplotlib figure.
* `**kwargs`: all keyword arguments will be passed on to plt.plot

Returns
--------
* the return from plt.plot

Raises
--------
* ImportError: if matplotlib dependency is not met.
