# Computer Vision DC | IIT Jodhpur

Study notes, Python implementations, and experiments for my Computer Vision DC at the Indian Institute of Technology Jodhpur (IITJ).

The preparation roadmap is based on **List of Topics for Preparing for CV-ML Research.pdf**. It progresses from image processing and classical machine learning to deep learning and modern vision models. All checklist items begin unchecked; they track planned work, not completed implementations.

## Objectives

- Understand the mathematical foundations of image processing and computer vision.
- Implement core techniques in Python and explain their behavior through experiments.
- Compare classical feature-based methods with learned representations.
- Develop reproducible experiments and maintain clear notes for DC discussions.

## Preparation roadmap

Related and repeated topics from the handout are grouped below. Spelling is standardized, including Hough transform and connected component labeling.

### 1. Image processing and computer vision

#### Image fundamentals and manipulation

- [ ] Image representation and spatial-domain operations.
- [ ] Read, display, and write images.
- [ ] Convert color images to grayscale and binary images.
- [ ] Flip images horizontally and vertically, crop regions, and rotate images.
- [ ] Compute image negatives and differences between two images.
- [ ] Flatten images into vectors and explore row-major and column-major ordering.
- [ ] Use Pillow (PIL) for image manipulation.

#### Filtering, derivatives, and geometry

- [ ] Mean, Gaussian, and median filters; mean and median statistics.
- [ ] Image gradients, Laplacian, and Laplacian of Gaussian.
- [ ] Line, corner, and edge detection.
- [ ] Hough transform and its properties.
- [ ] Linear, bilinear, and spline interpolation.
- [ ] Add different types of noise and compare noise removal methods.

#### Intensity transformations and segmentation

- [ ] Image histograms, histogram equalization, matching, and normalization.
- [ ] Histogram-based thresholding and Otsu's algorithm.
- [ ] Linear and piecewise-linear intensity transformations, gamma correction, and contrast stretching.
- [ ] Morphological operations.
- [ ] Foreground/background segmentation using image processing techniques without ML or DL.
- [ ] Graph cut and GrabCut segmentation.
- [ ] Connected component labeling.

#### Vector similarity and distance

- [ ] Cosine and sine distance between flattened image vectors, as listed in the handout; document the definitions used.
- [ ] Euclidean norm and its relationship to Euclidean distance.
- [ ] Geodesic, Manhattan, and Minkowski distances.

### 2. Classical machine learning

- [ ] k-nearest neighbors (k-NN) and minimum distance classifiers.
- [ ] Linear regression, nonlinear regression, and logistic regression.
- [ ] Support vector machines and random forests.
- [ ] Feature extraction and classification pipelines.
- [ ] Principal component analysis (PCA).
- [ ] k-means, k-medoids, hierarchical clustering, and DBSCAN.
- [ ] Local binary patterns (LBP) and histogram of oriented gradients (HOG).
- [ ] Bag of Words; study the Bag of Visual Words formulation for image tasks.

### 3. MNIST mini-project

Implement the handout's mini-project on handwritten digit classification:

- [ ] Perform data augmentation.
- [ ] Extract features using PCA, LBP, and HOG.
- [ ] Train a logistic regression classifier.
- [ ] Classify extracted features using methods such as random forests.
- [ ] Explore a Bag of Visual Words representation.

Suggested experiment practice:

- Use a fixed train/validation split and reserve the test set for final evaluation.
- Apply augmentation to training data only; fit preprocessing and feature transformations on training data.
- Compare raw-pixel, PCA, LBP, and HOG representations under a consistent evaluation setup.
- Record accuracy, per-class results, a confusion matrix, and representative errors.
- Document descriptor choices and limitations when adapting Bag of Visual Words to MNIST.

### 4. Deep learning with PyTorch

#### Foundations

- [ ] PyTorch basics: tensors, autograd, datasets, data loaders, and training loops.
- [ ] Perceptrons, multilayer perceptrons, and universal approximation.
- [ ] Learning and risk minimization; gradient descent and backpropagation.
- [ ] Loss functions and how to choose them.
- [ ] Batch size, stochastic gradient descent, mini-batch methods, and second-order methods.
- [ ] Optimizers, regularization, batch normalization, and dropout.

#### Core architectures and interpretation

- [ ] Convolutional neural networks: vision models, architecture, and training.
- [ ] CNN layer visualization, Grad-CAM, and t-SNE plots.
- [ ] Transposed convolution.
- [ ] Autoencoders, convolutional autoencoders, and denoising autoencoders.
- [ ] RNNs, LSTMs, and GRUs.

#### Vision tasks

- [ ] Image classification: ResNet, VGG, DenseNet, and MobileNet.
- [ ] Object detection: R-CNN, Fast R-CNN, Faster R-CNN, Mask R-CNN, Grid R-CNN, SSD, and YOLO.
- [ ] Image segmentation: SegNet and U-Net.

#### Generative and foundation models

- [ ] Variational autoencoders (VAEs) and generative adversarial networks (GANs).
- [ ] DCGAN and CycleGAN.
- [ ] Diffusion models.
- [ ] Attention and transformers.
- [ ] Vision Transformer (ViT), Swin Transformer, and DINOv2 for image classification.
- [ ] Transformer-based segmentation, including TransUNet and Swin-Unet.
- [ ] Transformer-based object detection.

## Suggested repository structure

This is a proposed organization for future work; the folders and implementations are not included with this README.

```text
.
|-- README.md
|-- notes/                  # Concepts, derivations, and paper summaries
|-- notebooks/
|   |-- image_processing/
|   |-- machine_learning/
|   `-- deep_learning/
|-- src/                    # Reusable implementations
|-- experiments/
|   `-- mnist/              # Configurations, scripts, and experiment records
|-- results/                # Metrics, plots, and selected outputs
|-- reports/                # DC progress summaries and presentations
`-- requirements.txt       # Dependencies and versions once established
```

## Working approach

For each topic:

1. Write a short explanation with the main equations and assumptions.
2. Implement the method and compare with a library implementation where useful.
3. Run a small experiment with clearly stated inputs and parameters.
4. Save representative outputs and explain successes, failures, and limitations.
5. Mark the topic complete when the notes, code, and observations are ready for discussion.

For reproducible experiments, record the dataset split, random seed, preprocessing, model configuration, dependency versions, and evaluation metrics. Add executable setup and run commands as implementations become available.

## DC progress log

| Date | Topic / experiment | Evidence / result | Questions and next steps |
| --- | --- | --- | --- |
| To be added | | | |

## Reference material

Primary scope reference: **List of Topics for Preparing for CV-ML Research.pdf**, supplied for preparation. The checklist above organizes its topics; the workflow, repository structure, and evaluation suggestions are additions for managing the work, not stated IITJ requirements.

Selected learning links reproduced from the handout:

- [Digital Image Processing using Python](https://www.youtube.com/watch?v=zDWJUSeuiZs&list=PLx3nvcXDbLZPvTKFuyxQ-A847SWbQrsts)
- [Image Processing using OpenCV](https://www.youtube.com/watch?v=oUJs03eZ0S8&list=PLKnIA16_RmvYXDBJ5WRDuQRSzFJs93pYR&index=1)
- [CMU Machine Learning course](https://www.cs.cmu.edu/~mgormley/courses/10601/)
- [Stanford CS229](https://cs229.stanford.edu/)
- [PyTorch tutorials](https://pytorch.org/tutorials/)
- [CMU Deep Learning course, Fall 2024](https://deeplearning.cs.cmu.edu/F24/index.html)
- [Stanford CS231n](https://cs231n.stanford.edu/)
- [Stanford CS230 syllabus](https://cs230.stanford.edu/syllabus/)

These links are taken from the supplied document and have not been independently checked for availability.
