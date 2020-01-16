### [MVHistogram](MVHistogram.md).to_histogram (method)


```py

def to_histogram(self, N=1000, bins=10, range=None, dimension=None)

```



Convert the [MVHistogram](MVHistogram.md) distribution to a [Histogram](Histogram.md) distribution.

Under-the-hood, this calls [MVHistogram.sample](MVHistogram.sample.md) with `size=N` and `wrap_at=False`
and passes the resulting array as well as the requested `bins` and `range`
to [Histogram.from_data](Histogram.from_data.md).

Arguments
-----------
* `N` (int, optional, default=1000): number of samples to use for
    the histogram.
* `bins` (int, optional, default=10): number of bins to use for the
    histogram.
* `range` (tuple or None): range to use for the histogram.
* `dimension` (int or string, default=None): dimension to use
    when flattening to the 1-D histogram distribution. If not proivded
    or None, will use value from [MVHistogram.dimension](MVHistogram.dimension.md).  `dimension` is
    therefore REQUIRED if [MVHistogram.dimension](MVHistogram.dimension.md) is None.

Returns
--------
* a [Histogram](Histogram.md) object

Raises
---------
* ValueError: if `dimension` and [MVHistogram.dimension](MVHistogram.dimension.md) are both None.
