# VPEX
VeriSilicon's PyTorch EXtension

## Preparation
```shell
pip install vpex-0.7.0-cp310-cp310-linux_x86_64.whl
export LD_LIBRARY_PATH=your_env/lib/python3.x/site-packages/vpex/lib:$LD_LIBRARY_PATH
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