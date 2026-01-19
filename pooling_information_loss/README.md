# Pooling-Induced Information Loss in Vision Models

## Research Question
How do different pooling operations affect information preservation in convolutional neural networks?

## Method
A controlled convolutional architecture is used where the pooling operation is the only variable. Max pooling and average pooling are compared by measuring feature variance across spatial dimensions of intermediate representations using CIFAR-10 inputs.

## Results
Max pooling yields significantly higher feature variance than average pooling, indicating stronger preservation of salient activations. Average pooling produces smoother, lower-variance feature maps, suggesting greater information compression.

## Interpretation
The observed variance gap reflects a fundamental invariance–information trade-off. Max pooling emphasizes discriminative local responses, while average pooling enforces spatial smoothing that increases invariance but reduces representational richness.

## Limitations
- Analysis is limited to a shallow convolutional network.
- Feature variance is used as a proxy for information content.
- Downstream task performance is not evaluated.

## Future Work
Future experiments could study pooling effects across depth, incorporate additional pooling strategies, and relate representation variance to robustness and generalization in downstream tasks.
