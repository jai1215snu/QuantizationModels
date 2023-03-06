# QuantizationModels
The purpose of this repository is to provide a summary of papers on quantization.

## Papers

**Keywords**: **`qnn`**: quantized neural networks | **`bnn`**: binarized neural networks | **`hardware`**: hardware deployment | __`other`__

### 2022
- [__` `__][[CVPR](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhong_IntraQ_Learning_Synthetic_Images_With_Intra-Class_Heterogeneity_for_Zero-Shot_Network_CVPR_2022_paper.pdf)] IntraQ: Learning Synthetic Images with Intra-Class Heterogeneity for Zero-Shot Network Quantization [**`qnn`**] [[code](https://github.com/zysxmu/IntraQ)]
- [__`V`__][[CVPR](https://arxiv.org/abs/2111.14826)] Nonuniform-to-Uniform Quantization: Towards Accurate Quantization via Generalized Straight-Through Estimation. [**`qnn`**] [[code](https://github.com/liuzechun/Nonuniform-to-Uniform-Quantization)] [59⭐]
  - `NonLinear` | `QAT` | 
  - New STE(for non-linear)
  - Weight/Feature data normalization is used to achieve equal quantization values.
- [__`V`__][[CVPR](https://openaccess.thecvf.com/content/CVPR2022/papers/Jeon_Mr.BiQ_Post-Training_Non-Uniform_Quantization_Based_on_Minimizing_the_Reconstruction_Error_CVPR_2022_paper.pdf)] Mr.BiQ: Post-Training Non-Uniform Quantization based on Minimizing the Reconstruction Error.  [__`qnn`__]
  - `NonLinear` : 몇개의 alpha 값을 찾아서 해당 값의 +-1 에 해당하는 bit로 quantization을 수행
  - `PTQ` : without data
  - `LayerReconstruction` : Layer의 출력을 student, teacher로 학습하여 최대한 유지하도록 학습
  - BREQ와 닮은 점이 있다.(Breq는 linear quant.인 반면 Mr.BiQ는 non linear)

### 2021
- [__`V`__][[AAAI](https://arxiv.org/abs/1909.05840)] [[code](https://github.com/sIncerass/QBERT)] Q-BERT: Hessian Based Ultra Low Precision Quantization of BERT.  [__`qnn`__]
  - `Hessian/Eigen` | `GroupQuant` | `QAT` | `STE` | `MixedQuant`
- [[ICLR](https://openreview.net/forum?id=POWv6hDd9XH)] BRECQ: Pushing the Limit of Post-Training Quantization by Block Reconstruction. [__`qnn`__] [[torch](https://github.com/yhhhli/BRECQ)]

### TBD
-  Pact: Parameterized clipping activation for quantized neural networks.
- ADDITIVE POWERS-OF-TWO QUANTIZATION: AN EFFICIENT NON-UNIFORM DISCRETIZATION FOR NEURAL NETWORKS
