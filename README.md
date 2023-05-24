## 1. 项目描述

本项目为 yolov5 可视化界面，基于 PyQt5 开发。

## 2. 安装

克隆本项目到本地：

```bash
git clone https://github.com/aifyb/yolov5_gui.git
```

安装依赖：

```bash
pip install -r requirements.txt
```

## 3. 使用

1. 导出网络模型文件的onix 或 torchscript 格式：
    
    ```bash
    python export.py --data data.yaml --weights yolov5s.pt --img 640 --include torchscript --device cuda:0
    python export.py --data data.yaml --weights yolov5s.pt --img 640 --include onnx --opset 13
    ```
2. 修改本项目下的 `model.yaml` 文件，将 `model_path` 修改为导出的模型文件路径，`names` 修改为你数据集的类别名称，`imgsz` 修改为你训练时的图片尺寸。
3. 运行 `run_gui.py` 文件，即可打开可视化界面，见名知意，不再赘述。

## 4. 参考
b站up主魔傀面具：https://space.bilibili.com/286900343