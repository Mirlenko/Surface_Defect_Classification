# Computer Vision Applications for Industry 4.0

In the current project one of the possible __Computer Vision__ applications for __Industry 4.0__ is reviewed and simulated.

__The data__ used is 1800 images of six typical steel defects (the classes are balanced): crazing, inclusion, patches, pitted surface, rolled-in scale and scratches. Each defect has its own patterns, that were proved to be recognized by the NN with high accuracy (_val_accuracy_ equaling ?).

__The Convolutional Neural Network (CNN)__ used for defects classification is [_ResNet101_](https://arxiv.org/abs/1512.03385) architecture. 

In order to not replicate the original ResNet architecture presented in the paper, the _Transfer Learning_ technique is used. The _keras_ framework has ResNet implementation, that can be used in _tensorflow_. However, the only the layers order and parameters are remained in an original way, as the weights calculated for each neuron based on Imagenet dataset are not suitable for the steel strip surface images used in the current project. For this reason, the NN is fitted on the 70% dataset; the remaining 30% is used for validation purposes. At the top of the net the fully-connected layer is built to output the predicted defect class. 

The project work is inspired by the original paper [An End-to-End Steel Surface Defect Detection Approach via Fusing Multiple Hierarchical Features](https://ieeexplore.ieee.org/document/8709818).
