# promo_plot
 Corner plots -- now with ads!

# Installation

via git clone:
```
pip install promo_plot/
```

# Usage

```
from promo_plot import promo_plot

# Generate fake data
df = pd.DataFrame(
    np.random.normal(1, 0.5, size=(1000, 6)),
    columns=[f'col{i+1}' for i in range(6)]
)

kwargs = dict(
        hist_kwargs=dict(lw=3, color='black'),
        labels = df.columns,
        quantiles=[0.5],
        label_kwargs=dict(fontsize=22))

fig = promo_plot(df, **kwargs)
```

Add your own ads! Drop a png or jpeg in the ``ad_images'' folder. Works best for equal-aspect or 2:1 aspect images.
