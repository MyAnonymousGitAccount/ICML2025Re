Comparison of LPIPS scores across different methods and masking settings. The evaluation follows the same setup as in the our paper. For fair comparison, we evaluate DPS and CoPaint using their default configurations with 20-step diffusion sampling. CoPaint-2 and CoPaint-3 (using 2 and 3 gradient descent steps respectively) have comparable runtime to LanPaint-5 and LanPaint-10. LanPaint achieves the best performance in all scenarios. (C means Celebra-A, I means Imagenet, CB means checker board)
| Method/Task     | C-Box | C-Half | C-CB | I-Box | I-Half | I-CB |
|-----------------|---------------|----------------|--------------|---------------|----------------|--------------|
| CoPaint-2         | 0.179         | 0.345          | 0.316        | 0.235         | 0.379          | 0.228        |
| CoPaint-3         | -         | -          | -        | 0.227         | 0.371          | 0.276        |
| DPS             | 0.125         | 0.281          | 0.212        | 0.208         | 0.352          | 0.303      |
| LanPaint-5 (BiG+FLD) | 0.105 | 0.277 | 0.190 | 0.197 | **0.337** | 0.147 |
| LanPaint-10 (BiG+FLD) | **0.103** | **0.277**      | **0.189**    | **0.193**     | 0.338     | **0.128**    |

Note that divergence occurs on ImageNet due to the pre-trained model's scaled linear noise schedule (vs. CelebA's linear schedule), requiring step size adjustments. The results show that FLD is stable for both cases.
