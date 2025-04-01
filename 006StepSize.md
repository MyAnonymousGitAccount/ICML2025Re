##### Caption: Performance comparison between reduced step size (0.03 on Box, 0.04 on Checkerboard) VS fixed step size (0.06, consistent with CelebA) on ImageNet. Langevin sampling exhibits $\color{red}{divergence}$  (LPIPS Langevin-10 > Langevin-5 > Replace) for Box at step size 0.06, while LanPaint variants maintain superior results across different step sizes.

| Method                      | ImageNet Box (reduced) | ImageNet Checkerboard (reduced) | ImageNet Box (0.06) | ImageNet Checkerboard (0.06) |
|-----------------------------|--------------|------------------------|---------------------|-------------------------------|
| Langevin-10                 | 0.221        | 0.231                 | $\color{red}{0.279}$         | 0.236                  |
| Langevin-5                  | 0.226        | 0.314                 | $\color{red}{0.262}$                   |0.307
| Replace¶                    | 0.228       | 0.405                 | $\color{red}{0.228}$                  |0.405
| **LanPaint-5 (BiG score)**  | 0.212        | 0.183                 | 0.248          | 0.178                   |
| **LanPaint-10 (BiG score)** | 0.209        | 0.151                 | 0.266         | 0.156                   |
| **LanPaint-5 (FLD)**        | 0.211        | 0.214                 | 0.213          | 0.185                   |
| **LanPaint-10 (FLD)**       | 0.203        | 0.158                 | 0.215          | 0.141                  |
| **LanPaint-5 (BiG+FLD)**    | 0.197        | 0.147                 | **0.200**          | 0.137                   |
| **LanPaint-10 (BiG+FLD)**   | **0.193**    | **0.128**             | 0.212      | **0.123**               |

Note that divergence occurs on ImageNet due to the pre-trained model's scaled linear noise schedule (vs. CelebA's linear schedule), requiring step size adjustments. The results show that LanPaint is stable for both cases.
