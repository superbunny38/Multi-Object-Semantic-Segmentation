# Multi-Object-Semantic-Segmentation

**Task**: Segment Left and Right Lung from Lung Dataset

# Data
![img_mask](https://user-images.githubusercontent.com/48243487/178134605-5ad3dcfd-fabe-40f8-b654-49ed43f70586.JPG)

(Contact me via e-mail if you need segmented data)

## Pre-processing Images



## Models
- PSPNet
- ResNet101


## Post-processing

## Results

| Model (epoch) | Augmentation  | Average Dice Coefficient (on Test score) |
| -------------| ------------- | ------------- |
| PSPNet (epoch: 50) | Random Mirror (num. of train imgs: 794)  | mean dice: 0.9425 (left lung 0.9538, right lung: 0.9312)  |
| PSPNet (epoch: 25) | Cutmix (num. of train imgs: 367) | mean dice:  0.9501 (left lung: 0.9622, right lung: 0.9380) |
| PSPNet (epoch: 30)  | Albumentation1 (num. of train imgs: 367)  | mean dice: 0.9473 (left lung:0.9601 right lung: right lung: 0.9345)  |
| PSPNet (epoch: 25)  | Cutout  | 0.905  |
| SpiralNet-ResNet  | 0.905  | 0.905  |
| SpiralNet-ResNet  | 0.905  | 0.905  |
