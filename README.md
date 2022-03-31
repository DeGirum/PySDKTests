# PySDKExamples
DeGirum PySDK Examples

## Installation

It is recommended to install the degirum package inside a virtual environment. Currently, Python3.8 is supported. Other versions will be supported in future.


To install DeGirum PySDK from the DeGirum index server use the following command:

```
python -m pip install degirum --extra-index-url https://degirum.github.io/simple
```

To force reinstall the most recent PySDK version without reinstalling all dependencies use the following command:
```
python -m pip install degirum --upgrade --no-deps --force-reinstall --extra-index-url https://degirum.github.io/simple
```

## Quick Start
```python
import degirum as dg

image_url="https://raw.githubusercontent.com/degirum/DeGirum.github.io/master/images/samples/cat_640.jpg"
zoo = dg.connect_model_zoo()
mobilenet_ssd = zoo.load_model("mobilenet_v2_ssd_coco--300x300_quant_n2x_orca_1")
result = mobilenet_ssd(image_url)
print(result)
result.image_overlay.show()
```
