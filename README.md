# Why the rich keep getting richer

An interactive model of wealth inequality. The same population of households is replayed twice, with the same starting wealth and the same run of luck. Only one thing differs: how much wealth is redistributed each year. Watch where the wealth goes.

Live page: https://jksteel.github.io/Inequality/

## The model

It's the Bouchaud–Mézard model (Physica A, 2000). Each household's wealth compounds at the same average rate, with its own random good and bad years. A redistribution term pulls everyone towards the average:

```
dw = m·w·dt + σ·w·dW + J·(mean − w)·dt
```

| Symbol | Meaning | Default |
|---|---|---|
| `m` | Average growth rate | 2%/yr |
| `σ` | Volatility of returns (luck) | 19.5% |
| `J` | Redistribution rate | 1.9%/yr (left), 0.8%/yr (right) |

In the long run the richest households follow a Pareto tail with exponent `μ = 1 + 2J/σ²`.

**Tipping point.** Below `J = σ²/2` (μ = 2), the spread of wealth keeps growing; above it, the spread settles. The two default `J` values come from US wealth data: μ ≈ 2.0 in 1978 and μ ≈ 1.4 in 2012 (Saez & Zucman, 2016).

The page's key and reference list give the full sourcing.

## Files

| Path | What it is |
|---|---|
| `index.html` | The page (served as the live site) |
| `preview.png` | Social-media preview image |
| `LICENSE` | Public domain (Unlicense) |

## Running it

`index.html` is a single self-contained file with no dependencies or build step. Open it in a browser.

## Licence

The code and text are released into the public domain under the [Unlicense](LICENSE). The papers it cites belong to their publishers.
