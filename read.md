# Acheiving 99.4% accuracy in MNIST in a HIGHLY resource constrained system
---
## Constraints:
- Parameters should be less than 10,000
- Accuracy to be achieved in less than 15 epochs
## Progress in this notebook
- Since I had already done some iterations in the previous [assignment](https://github.com/sairamsubramaniam/tsai_projects/tree/master/assignment2_MNIST), the easiest way to start was to take the previous model, reduce parameters to below 10k and see how the model performed.
- The model gave an accuracy of 99.27% (**99.21%** avg in last 5 epochs) with just **6,246** params in **20** epochs
## The model consists of:
- Contains 8 layers with following number of kernels:
  - Conv 8 -> Conv 8 -> Bottlenck -> Conv 16 -> Conv 16 -> Conv 8 -> Conv 0 -> GAP
  - Bottleneck layer = Maxpool + 1x1 Conv
- Only 3x3 convolution used everywhere (except for the bottleneck & GAP layers
- Except the bottleneck & last Conv layer, every convolution is followed by "RELU" & "Batch Normalization"
- No padding has been used anywhere