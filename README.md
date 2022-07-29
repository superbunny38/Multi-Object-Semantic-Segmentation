# Multi-Object-Semantic-Segmentation

**Task**: Segment Left and Right Lung from Lung Dataset

**Presentation link**: https://docs.google.com/presentation/d/1gTv_T3emhZpL3ZO1yKkmYnJcfkhZl6ke1m0ANZmFM7g/edit#slide=id.g13c4dc079d2_0_356


# Data
![img_mask](https://user-images.githubusercontent.com/48243487/178134605-5ad3dcfd-fabe-40f8-b654-49ed43f70586.JPG)

(Contact me via e-mail if you need segmented data)

## Pre-processing Images



## Models
- PSPNet (Pyramid Scene Parsing Network)
- ResNet101

## FINAL MODEL
![image](https://user-images.githubusercontent.com/48243487/180593519-b9963bc2-9d92-448f-96eb-c4a14fba31d9.png)

- **Model: PSPNet (Pyramid Scene Parsing Network)**
- **Pretrained weights on: ADE20k**
- **Optimizer: Adam**
- **LR scheduler: Cosine Annealing**
- **Criterion : 0.01xSoft Dice Loss + 0.99xBoundary Loss + 0.3xAuxiliary Loss**
- **Performance: 0.98 dice on test set**


## Results

| Model (epoch) | Augmentation  | Average Dice Coefficient (on Test score) | model link |
| -------------| ------------- | ------------- |------------- |
| PSPNet (epoch: 50) | Random Mirror (num. of train imgs: 794)  | mean dice: 0.9425 (left lung 0.9538, right lung: 0.9312)  ||
| PSPNet (epoch: 25) | Cutmix (num. of train imgs: 367) | mean dice:  0.9501 (left lung: 0.9622, right lung: 0.9380) ||
| PSPNet (epoch: 30)  | Albumentation1 (num. of train imgs: 367)  | mean dice: 0.9473 (left lung:0.9601 right lung: 0.9345)  ||
| PSPNet (epoch: 25)  | Cutout (num. of train imgs: 367)  | mean dice: 0.4597 (left lung: 0.2758, right lung: 0.6436)  ||
| PSPNet pretrained on cutmix (25) (epoch: 10) + HD losss  | None  | mean dice: 0.613  (left lung: 0.5941 right lung: 0.6328)||
| PSPNet pretrained on cutmix (25) (epoch: 10) + minimized HD losss + increased weight decay + decreased lr | None  | mean dice: 0.9554 (left lung: 0.9645 right lung: 0.9464 ) ||
| PSPNet pretrained on cutmix (25) (epoch: 25) + minimized HD losss + increased weight decay + decreased lr | None  | mean dice: 0.9555 (left lung 0.9645 right lung: 0.9464 ) ||
| PSPNet pretrained on cutmix (25) (epoch: 5) + minimized BD losss + trainable weights on loss | Histogram equalizer | mean dice: 0.9612 (left lung 0.9671 right lung: 0.9553 ) | [link](https://drive.google.com/file/d/1fRMiIs_Zr4sttBKXyLjqcyIGA5in-MBf/view?usp=sharing) |
| PSPNet pretrained on cutmix (25) (epoch: 10) + weighted DC + BD| Histogram equalizer | mean dice: 0.9498 (left lung 0.9560 right lung: 0.9436 )  ||
| PSPNet Cosine Annealing (epoch: 50) + DC + BD| Histogram equalizer | mean dice: **0.98** (left lung: 0.98141 right lung: 0.97686) |[link](https://drive.google.com/file/d/10_oTVDqIdSfH2eoml8gqS6XgmamkCTBF/view?usp=sharing)|


# Contact

**If you need codes or have any issue, please contact me via e-mail (superbunny38 at gmail dot come) with your needs.**
