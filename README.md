# This fork

This project is a fork of the main [ctcdecode](https://github.com/parlance/ctcdecode) project. This fork provides an implementation that works on Windows operating systems.

# ctcdecode

ctcdecode is an implementation of CTC (Connectionist Temporal Classification) beam search decoding for PyTorch.
C++ code borrowed liberally from Paddle Paddles' [DeepSpeech](https://github.com/PaddlePaddle/DeepSpeech).
It includes swappable scorer support enabling standard beam search, and KenLM-based decoding.

## Installation
The library is largely self-contained and requires only PyTorch 1.0. Building the C++ library requires gcc or clang. KenLM language modeling support is also optionally included, and enabled by default.

```bash
# get the code
git clone --recursive https://github.com/jtdremann/ctcdecode.git
cd ctcdecode

# Install PyTorch and torchvision first: https://pytorch.org/

# For Windows using MSVC compiler, you must modify the following Pytorch file:
# Lib/site-packages/torch/lib/include/csrc/api/include/torch/torch.h
# Modify (or remove) the lines:
# #warning "<text>"
# to:
# #pragma message ("<text>")

# Install wget
pip install wget

# Install ctcdecode
python setup.py install
```
