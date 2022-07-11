# Multi-Object-Semantic-Segmentation

**Task**: Segment Left and Right Lung from Lung Dataset

# Data
![img_mask](https://user-images.githubusercontent.com/48243487/178134605-5ad3dcfd-fabe-40f8-b654-49ed43f70586.JPG)

(Contact me via e-mail if you need segmented data)

## Pre-processing Images

**Random Mirror**

![mirrored](https://user-images.githubusercontent.com/48243487/178175680-3b83e63b-9899-4ad6-9544-93705cafa15a.JPG)


**Cutmix**

![cutmix](https://user-images.githubusercontent.com/48243487/178175759-057a0f29-b731-449e-8eed-fc87d8fefde8.JPG)


## Models
- PSPNet
- ResNet101


## Post-processing

## Results

| Model (epoch) | Augmentation  | Average Dice Coefficient (on Test score) |
| -------------| ------------- | ------------- |
| PSPNet (epoch: 50) | Random Mirror (num. of train imgs: 794)  | mean dice: 0.9425 (left lung 0.9538, right lung: 0.9312)  |
| RseNet101 | 0.865  | 0.865  |
| EfficientNet  | 0.914  | 0.914  |
| SpiralNet-ResNet  | 0.905  | 0.905  |
