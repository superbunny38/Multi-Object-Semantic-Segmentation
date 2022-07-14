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

| Model (epoch) | Augmentation  | Average Dice Coefficient (on Test score) | model link |
| -------------| ------------- | ------------- |------------- |
| PSPNet (epoch: 50) | Random Mirror (num. of train imgs: 794)  | mean dice: 0.9425 (left lung 0.9538, right lung: 0.9312)  ||
| PSPNet (epoch: 25) | Cutmix (num. of train imgs: 367) | mean dice:  0.9501 (left lung: 0.9622, right lung: 0.9380) ||
| PSPNet (epoch: 30)  | Albumentation1 (num. of train imgs: 367)  | mean dice: 0.9473 (left lung:0.9601 right lung: 0.9345)  ||
| PSPNet (epoch: 25)  | Cutout (num. of train imgs: 367)  | mean dice: 0.4597 (left lung: 0.2758, right lung: 0.6436)  ||
| PSPNet pretrained on cutmix (25) (epoch: 10) + HD losss  | None  | mean dice: 0.613  (left lung: 0.5941 right lung: 0.6328)||
| PSPNet pretrained on cutmix (25) (epoch: 10) + minimized HD losss + increased weight decay + decreased lr | None  | mean dice: 0.9554 (left lung: 0.9645 right lung: 0.9464 ) ||
| PSPNet pretrained on cutmix (25) (epoch: 25) + minimized HD losss + increased weight decay + decreased lr | None  | mean dice: 0.9555 (eft lung 0.9645 right lung: 0.9464 ) ||
| PSPNet pretrained on cutmix (25) (epoch: 5) + minimized BD losss + trainable weights on loss | Histogram equalizer | mean dice: 0.9555 (eft lung 0.9645 right lung: 0.9464 ) |mean dice: 0.961 (left lung 0.967 right lung: 0.955)| link(https://drive.google.com/file/d/1fRMiIs_Zr4sttBKXyLjqcyIGA5in-MBf/view?usp=sharing ) |
