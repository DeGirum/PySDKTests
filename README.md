# PySDKExamples
DeGirum PySDK Examples

## Installation

Prerequisites: 
1. Python 3.8 should be installed in your system and configured to be the default Python installation or
2. Virtual environment with Python 3.8


To install DeGirum PySDK from the DeGirum index server use the following command:

```
python -m pip install degirum --extra-index-url https://DeGirum.github.io/simple
```

To force reinstall the most recent PySDK version without reinstalling all dependencies use the following command:
```
python -m pip install degirum --upgrade --no-deps --force-reinstall --extra-index-url https://DeGirum.github.io/simple
```

## Quick Start
```python
import degirum as dg

image_url="https://raw.githubusercontent.com/degirum/DeGirum.github.io/master/images/samples/cat_640.jpg"
zoo = dg.connect_model_zoo()
mobilenet_ssd = zoo.load_model("ssd_mobilenet_v2--300x300_quant_n2x_orca_1")
result = mobilenet_ssd(image_url)
print(result)
result.image_overlay.show()
```
