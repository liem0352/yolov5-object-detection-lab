# YOLOv5目标检测实训

## 项目简介
本项目基于 YOLOv5 目标检测框架，对不同场景下的图片进行目标检测实践。包含多组测试图片和对应的检测结果可视化，涵盖街道、室内、自然场景等多种环境。

## 项目结构
```
├── test_images/          # 测试输入图片
│   ├── street_scene1.jpg     # 街道场景1
│   ├── street_scene2.jpg     # 街道场景2
│   ├── new_scene1.jpg        # 新场景1
│   ├── new_scene2.jpg        # 新场景2
│   ├── scene3.jpg            # 场景3
│   ├── scene4.jpg            # 场景4
│   ├── new_image1.jpg        # 测试图片1
│   └── new_image2.jpg        # 测试图片2
├── results/              # 检测结果图片
│   ├── result_bus.jpg        # 公交车检测结果
│   ├── result_zidane.jpg     # 人物检测结果
│   ├── result_bedroom.jpg    # 卧室场景检测结果
│   ├── result_forest.jpg     # 森林场景检测结果
│   ├── result_restaurant.jpg # 餐厅场景检测结果
│   ├── result_new11.jpg      # 新场景1检测结果
│   └── result_new22.jpg      # 新场景2检测结果
└── README.md             # 项目说明
```

## 技术栈
- YOLOv5 (Ultralytics)
- PyTorch
- Python 3.13
- CUDA (GPU加速，可选)

## 实训内容

### 1. 环境搭建
- 安装 YOLOv5 依赖
- 下载预训练权重 (yolov5s.pt)
- 配置 Python 环境

### 2. 目标检测实践
使用 YOLOv5 预训练模型对不同场景图片进行目标检测：
- **街道场景**：检测行人、车辆、交通标志等
- **室内场景**：检测家具、电器、人物等
- **自然场景**：检测动物、植物等

### 3. 检测结果分析
- 分析不同场景下的检测准确率
- 对比不同目标的检测置信度
- 评估模型在各类场景中的表现

## 使用方法

### 安装依赖
```bash
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
pip install -r requirements.txt
```

### 运行检测
```bash
python detect.py --weights yolov5s.pt --source path/to/image.jpg
```

### 查看结果
检测结果默认保存在 `runs/detect/exp/` 目录下。

## 检测示例

输入图片放在 `test_images/` 目录，对应的检测结果放在 `results/` 目录。可以通过对比两组图片来评估YOLOv5的检测效果。

## 注意事项
1. 本项目仅包含测试图片和检测结果，YOLOv5源码请从 [ultralytics/yolov5](https://github.com/ultralytics/yolov5) 获取
2. 检测结果使用 yolov5s 预训练权重生成
3. 图片仅供学习和参考使用

---
**作者**：liem
**框架**：YOLOv5
**模型**：yolov5s