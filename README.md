# Fork of [spacewalk01/yolov9-face-detection](https://github.com/spacewalk01/yolov9-face-detection)

Differences between original repository and fork:

* Compatibility with PyTorch >=2.4. (🔥)
* Original pretrained models and converted ONNX models from GitHub [releases page](https://github.com/clibdev/yolov9-face-detection/releases). (🔥)
* The following deprecations and errors has been fixed:
  * FutureWarning: You are using 'torch.load' with 'weights_only=False'.

# Installation

```shell
pip install -r requirements.txt
```

# Pretrained models

* Download links:

| Name         | Model Size (MB) | Link                                                                                                                                                                                                                              | SHA-256                                                                                                                              |
|--------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| YOLOv9c-Face | 390.7<br>193.9  | [PyTorch](https://github.com/clibdev/yolov9-face-detection/releases/latest/download/yolov9c-face-spacewalk01.pt)<br>[ONNX](https://github.com/clibdev/yolov9-face-detection/releases/latest/download/yolov9c-face-spacewalk01.pt) | 403bd148652e8c5cfd39ba4c3e4f631b85bb0ea2bc583e0907426acc25138d29<br>3ab8234da28b74a28015662a672d147cd60fb540082c3c88eea69aa387069136 |

# Inference

```shell
python yolov9/detect.py --weights yolov9c-face-spacewalk01.pt --source assets/worlds-largest-selfie.jpg
```

# Export to ONNX format

```shell
pip install onnx
```
```shell
python yolov9/export.py --weights yolov9c-face-spacewalk01.pt --include onnx
```
