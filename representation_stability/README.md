# Representation Stability of CNNs under Input Perturbations

## Research Question
How stable are convolutional neural network representations under controlled input perturbations?

## Method
We analyze representation stability in a pretrained ResNet-18 by measuring cosine similarity between clean and perturbed intermediate features. Gaussian noise with increasing standard deviation is applied to the input image. Feature embeddings are extracted from an early convolutional block (layer1) and a deeper block (layer3) using forward hooks, and similarity is computed relative to the clean baseline.

## Results
Representation similarity decreases monotonically as noise strength increases for both early and deep layers. Early-layer representations remain more stable under noise, while deeper representations show a sharper decline in similarity as perturbation strength grows.

## Interpretation
The results indicate a depth-dependent robustness trade-off in convolutional networks. While deeper layers provide abstraction and invariance under mild perturbations, they may be more vulnerable to representational collapse under severe input noise. This suggests that robustness properties vary across depth and are not uniformly distributed throughout the network.

## Limitations
- Experiments are conducted on a single pretrained architecture.
- Analysis focuses on Gaussian noise and does not include other perturbation types.
- Results are empirical and do not establish theoretical guarantees.

## Future Work
Future extensions include analyzing additional perturbations (blur, occlusion), comparing architectures with different normalization strategies, and studying how residual connections affect representation stability.
