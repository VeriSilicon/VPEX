# VPEX
VeriSilicon's PyTorch EXtension

## Preparation
There are two ways to install vpex here.
1. pip install from pypi
```shell
pip install vpex
pip install vpex -i https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple
```
2. pip install wheel
The wheel package can be obtained from https://pypi.org/project/vpex/ or releases page on Github.
```shell
pip install vpex-0.7.0-cp310-cp310-manylinux_2_34_x86_64.whl
```
## Usage
```python
import torch
import vpex

print ("VSI is available: ", torch.vsi.is_available())

A = torch.ones(3, 3, device='vsi')
B = torch.zeros(3, 3, device='vsi')
result = A + B
print(result.to('cpu'))
```