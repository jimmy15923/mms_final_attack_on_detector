# Adversarial-attack on modern object detectors
Evaluate the robustness of modern object detectors, e.g., YOLO, Faster R-CNN by given adversarial examples via FGSM and DeepFool algorithms.

## Requirements
```
pip install torch, mmdet
```


## Steps
1. Download  dataset by
```script
wget https://s3.amazonaws.com/fast-ai-imageclas/imagenette2.tgz
```

2. Extract the data and put it in the folder `./data/imagenette2/`

3. Preprocess
```python
python3 process.py
```
4. Train the classification model
```python
python3 train.py --model_name resnet50 
```
5. Generate adversarial examples by FGSM and DeepFool.
```
run.sh
```

6. Inferecern the original samples and adversarial adversarial by `inference.ipynb`
7. Visualize the inference results by `visualize.ipynb`
