Comparison of LPIPS scores across different methods and masking settings. The evaluation follows the same setup as in the our paper. For fairness, DPS and CoPaint use their default configurations but with 20-step diffusion sampling for inference. LanPaint-10 (BiG+FLD) achieves the best LPIPS performance in all scenarios. (C means Celebra-A, I means Imagenet, CB means checker board)
| Method/Task     | C-Box | C-Half | C-CB | I-Box | I-Half | I-CB |
|-----------------|---------------|----------------|--------------|---------------|----------------|--------------|
| CoPaint         | 0.160         | 0.309          | 0.264        | 0.235         | 0.379          | 0.228        |
| DPS             | 0.125         | 0.281          | 0.212        | 0.208         | 0.352          | 0.303      |
| LanPaint-10 (BiG+FLD) | **0.103** | **0.277**      | **0.189**    | **0.193**     | **0.338**      | **0.128**    |

Note that divergence occurs on ImageNet due to the pre-trained model's scaled linear noise schedule (vs. CelebA's linear schedule), requiring step size adjustments. The results show that FLD is stable for both cases.
