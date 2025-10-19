# ResNet-18 PyTorch Implementation

This repository contains a minimal, custom implementation of the ResNet-18 architecture using PyTorch. 
This structure focuses on the core concepts of residual learning, particularly how residual connection are made.

---

### The Core Component: ResNet_layer (Basic Block)
The ResNet_layer implements the basic residual block (2x Conv3x3).

Key Residual Concepts Implemented:
- Identity Shortcut: The input is added directly to the output of the two convolutional layers (out2 + out_shortcut).

- Downsampling via Stride: Spatial size reduction (56×56 → 28×28) is performed by setting the stride of the first Conv3x3 layer within the block to 2.

- Projection Shortcut: When either the channel depth or the spatial size changes, a 1x1 convolution (self.shortcut) with matching stride is used to align the dimensions of the input (X) with the output (F(X)) for the residual connection.

---

## Reference
He, K., Zhang, X., Ren, S., & Sun, J. (2016) [Read the paper here](https://arxiv.org/abs/1512.03385)

## Author
Muhammad Ali
