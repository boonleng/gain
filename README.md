# Normal vs Leveraged Gains

The notion that leveraged gain is a decaying return can be a concern to many investors. It is a conventional wisdom that leveraged ETF is not meant for a long-term buy-and-hold strategy. However, most illustrative examples only touch on a one-day gain follow by a one-day loss, resulting in net loss that shows that leveraged ETF results in a bigger loss.

For example,

```
      Normal - Gain (10%): $100 * 0.9 -> $90   Loss (10%): $90 * 1.1 -> $99
3x Leveraged - Gain (30%): $100 * 0.7 -> $70   Loss (30%): $70 * 1.3 -> $91
```
where 3x-leveraged investment result in a bigger loss.

Another (counter) example,
```
      Normal - Gain (10%): $100 * 0.9 -> $90   Loss (20%): $90 * 1.2 -> $108
3x Leveraged - Gain (30%): $100 * 0.7 -> $70   Loss (60%): $70 * 1.6 -> $112
```
which results in a gain. 

### Q: So how should one really think about this?

The first example has a compound gain of 0.9 x 1.1 = 0.99 (less than one) while the second example has a compound gain of 0.9 x 1.2 = 1.08 (more than one, quite significantly). One should question what happens when there is a healthy overall gain during that investment period? After all, a good ETF should have a collection of assets that produces a net gain.

The notebook `gain.ipynb` provides a simluation to examine various scenarios.

# Example Output

![ex1](fig1.png)
![ex2](fig2.png)

| # | Up Days | Normal Return | Leveraged Return | Extremes | Has Positve | Better? |
| --: | --: | :-: | :-: | --: | :-: | :-: |
| 1 |  55 (55.0%) | +16.00% | +41.40% | -7.9%, +71.8% | + | + |
| 2 |  56 (56.0%) | +16.00% | +40.96% | -29.6%, +41.0% | + | + |
| 3 |  58 (58.0%) | +16.00% | +44.53% | -27.6%, +57.8% | + | + |
| 4 |  56 (56.0%) | +16.00% | +43.36% | -15.0%, +43.4% | + | + |
| 5 |  55 (55.0%) | +16.00% | +43.47% | -31.8%, +51.5% | + | + |
| 6 |  54 (54.0%) | +16.00% | +38.76% | -44.0%, +38.8% | + | + |
| 7 |  53 (53.0%) | +16.00% | +40.85% | -5.4%, +65.6% | + | + |
| 8 |  58 (58.0%) | +16.00% | +40.77% | -33.9%, +44.5% | + | + |
| 9 |  58 (58.0%) | +16.00% | +43.30% | -26.7%, +92.4% | + | + |
| 10 |  56 (56.0%) | +16.00% | +37.13% | -14.5%, +103.7% | + | + |
| : | : | : | : | : | : | : |
||
| **Average** | **54.8 (54.8%)** | **+16.00%** | **+41.78%** | **-54.8%, +274.6%**<br/>**( -16.3%, +73.3% )** | **100.00%** | **100.00%** |

![ex3](fig4.png)
![ex3](fig5.png)
