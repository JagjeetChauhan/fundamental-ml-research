# Failure Mode Analysis of Vision Models

## Motivation

Modern vision models are typically evaluated using aggregate accuracy metrics, which obscure how and why models fail. This project aims to move beyond overall performance and systematically analyze the structure of model errors.

## Research Question

Do vision model failures occur randomly, or do they cluster into interpretable and recurring failure modes?

## Experimental Setup

A pretrained ResNet-18 model is evaluated on CIFAR-10 images. Misclassified samples are collected and manually inspected. Each failure case is assigned a dominant failure mode based on visual characteristics, using a simple and interpretable taxonomy.

## Failure Mode Taxonomy

Failures are categorized into the following dominant modes:

- **Scale**: Loss of discriminative features due to low effective resolution, blur, or unusual object scale.
- **Background**: Foreground objects blending with or being dominated by background textures and context.
- **Occlusion**: Partial visibility or atypical framing that removes key object cues.

Each failure is assigned a single dominant cause to maintain interpretability and consistency.

## Results

The failure mode distribution reveals that errors are not uniformly distributed:

- Scale-related failures account for the largest proportion of errors.
- Occlusion and background bias contribute substantially but less frequently.

This indicates that model errors arise from structured weaknesses rather than random noise.

## Interpretation

The dominance of scale-related failures suggests sensitivity to effective resolution and feature quality. Background bias highlights challenges in foreground–background separation, while occlusion-related errors reflect reliance on canonical object views.

These findings demonstrate that aggregate accuracy metrics hide meaningful error structure. Failure mode analysis provides actionable insights into model limitations that are not captured by standard evaluation protocols.

## Limitations

- Failure mode labeling is manual and subjective.
- Analysis is limited to a single architecture and dataset.
- The number of inspected failures is relatively small.

## Future Directions

Future work may extend this analysis to other architectures, tasks (e.g., detection and segmentation), and datasets, as well as explore automated failure categorization and representation-level explanations.
