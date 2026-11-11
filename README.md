# MTG_slider

Before/after slider for comparing two MTG FCI frames: Cloud Phase RGB with cold tops ≤ 220 K, 2026-07-15, 14:30 vs 14:40 UTC.

**▶ Live slider:** https://sladekd.github.io/MTG_slider/

[![View on nbviewer](https://img.shields.io/badge/view-nbviewer-orange)](https://nbviewer.org/github/Sladekd/MTG_slider/blob/main/compare_slider.ipynb)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sladekd/MTG_slider/blob/main/compare_slider.ipynb)

## Files

- `index.html`: standalone slider served by GitHub Pages. You can drag on the image, use the slider, or press ← / →.
- `compare_slider.ipynb`: the Colab version. Running it builds the same slider from any two image arrays.
- `images/`: the two frames.

## Why it's fast

The slider runs entirely in the browser using a CSS `clip-path` on the top image. Moving it doesn't re-plot anything with matplotlib.

## Use it with your own images (Colab)

Run the first cell of the notebook, then:

```python
display(HTML(compare_html(img1, img2)))
```

To save a shareable page instead:

```python
open("my_slider.html", "w").write(compare_html(img1, img2))
```
