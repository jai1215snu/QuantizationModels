# QuantizationModels
The purpose of this repository is to provide a summary of papers on quantization.

## Papers

**Keywords**: **`qnn`**: quantized neural networks | **`bnn`**: binarized neural networks | **`hardware`**: hardware deployment | __`other`__

### 2023
- [[ICLR](https://arxiv.org/abs/2210.17323)] GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers [[code](https://github.com/IST-DASLab/gptq)] [721⭐]
  - OBS를 기반으로 수행한다. Hessian을 2XX^T로 구하고, weight를 하나씩 quantization 하고 나머지를 업데이트 하는 방식이다.
  - cholesky, block 연산을 추가하여 속도를 빠르게 하였다.
    
### 2022
- [[NeurIPS](https://nips.cc/Conferences/2022/Schedule?showEvent=54407)] ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers. [__`qnn`__]
  - 읽는 중..
- [__`V`__][[CVPR](https://openaccess.thecvf.com/content/CVPR2022/papers/Zhong_IntraQ_Learning_Synthetic_Images_With_Intra-Class_Heterogeneity_for_Zero-Shot_Network_CVPR_2022_paper.pdf)] IntraQ: Learning Synthetic Images with Intra-Class Heterogeneity for Zero-Shot Network Quantization [**`qnn`**] [[code](https://github.com/zysxmu/IntraQ)]
  - `Linear` | `PTQ`
  - `Zero Image` : image을 생성하여 quantization 수행. 
  - 각 Class의 Image을 평균내어, 최대한 퍼지게 학습
- [__`V`__][[CVPR](https://arxiv.org/abs/2111.14826)] Nonuniform-to-Uniform Quantization: Towards Accurate Quantization via Generalized Straight-Through Estimation. [**`qnn`**] [[code](https://github.com/liuzechun/Nonuniform-to-Uniform-Quantization)] [59⭐]
  - `NonLinear` | `QAT` | 
  - New STE(for non-linear)
  - Weight/Feature data normalization is used to achieve equal quantization values.
- [__`V`__][[CVPR](https://openaccess.thecvf.com/content/CVPR2022/papers/Jeon_Mr.BiQ_Post-Training_Non-Uniform_Quantization_Based_on_Minimizing_the_Reconstruction_Error_CVPR_2022_paper.pdf)] Mr.BiQ: Post-Training Non-Uniform Quantization based on Minimizing the Reconstruction Error.  [__`qnn`__]
  - `NonLinear` : 몇개의 alpha 값을 찾아서 해당 값의 +-1 에 해당하는 bit로 quantization을 수행
  - `PTQ` : without data
  - `LayerReconstruction` : Layer의 출력을 student, teacher로 학습하여 최대한 유지하도록 학습
  - BREQ와 닮은 점이 있다.(Breq는 linear quant.인 반면 Mr.BiQ는 non linear)
- [__`V`__][[arxiv](https://arxiv.org/pdf/2211.10438.pdf)] SmoothQuant: Accurate and Efficient Post-Training Quantization for Large Language Models. [[code](https://github.com/mit-han-lab/smoothquant)] [387⭐]
  - Activation 과 Weight를 잘 조율하여 한쪽을 s만큼 낮추고 한쪽을 s만큼 높여서 가장 좋은 s를 찾아서 quantization 하기 쉽도록 만들어 준다.
- [__`V`__][[ICLR](https://arxiv.org/abs/2210.17323)] GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers [[code](https://github.com/IST-DASLab/gptq)] [721⭐]
  - 방법 확인중
  - LLM에 대해 Weight만 Quantization함(4bit)
- [[NeurIPS](https://nips.cc/Conferences/2022/Schedule?showEvent=54407)] ZeroQuant: Efficient and Affordable Post-Training Quantization for Large-Scale Transformers. [__`qnn`__]
- [[NeurIPS](https://nips.cc/Conferences/2022/Schedule?showEvent=53412)] Optimal Brain Compression: A Framework for Accurate Post-Training Quantization and Pruning. [__`qnn`__] [**`hardware`**]
### 2021
- [__`V`__][[AAAI](https://arxiv.org/abs/1909.05840)] [[code](https://github.com/sIncerass/QBERT)] Q-BERT: Hessian Based Ultra Low Precision Quantization of BERT.  [__`qnn`__]
  - `Hessian/Eigen` | `GroupQuant` | `QAT` | `STE` | `MixedQuant`
- [__`V`__][[ICLR](https://openreview.net/forum?id=POWv6hDd9XH)] BRECQ: Pushing the Limit of Post-Training Quantization by Block Reconstruction. [__`qnn`__] [[torch](https://github.com/yhhhli/BRECQ)]

### TBD
-  Pact: Parameterized clipping activation for quantized neural networks.
- Additive Powers-of-Two Quantization: An Efficient Non-uniform Discretization for Neural Networks
- Differentiable Soft Quantization: Bridging Full-Precision and Low-Bit Neural Networks
