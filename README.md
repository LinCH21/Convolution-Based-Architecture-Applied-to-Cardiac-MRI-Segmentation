## Convolutional Based Architecture Applied to Cardiac MRI Segmentation

Final project for EN.601.682 Machine Learning: Deep Learning, Fall 2023.

## Dataset

The [Automated Cardiac Diagnosis Challenge (ACDC) in MICCAI Challenge](https://www.creatis.insa-lyon.fr/Challenge/acdc/databases.html), obtained from $150$ patients. Each image consists of approximately 10 2D slices.

Image sizes exceeding $256$ were excluded, subsequently resizing the remaining images to $256\times256$ by padding with zeros. The voxel intensity of each image are normalized.

In the end, $2858$ images were obtained, which further divided into a training set comprising $80\%$, a validation set comprising $10\%$, and a test set comprising $10\%$.

## Result

| Class | Evaluation      | ConvDeconv      | U-Net           | GridNet         |
| ----- | --------------- | --------------- | --------------- | --------------- |
| LV    | Dice            | $0.90\pm0.020$  | $0.92\pm0.019$  | $0.92\pm0.018$  |
| LV    | Hausdorff Dist. | $7.15\pm4.47$   | $9.61\pm5.83$   | $6.86\pm4.56$   |
| RV    | Dice            | $0.74\pm0.0039$ | $0.78\pm0.0038$ | $0.80\pm0.0037$ |
| RV    | Hausdorff Dist. | $30.83\pm10.84$ | $25.50\pm9.72$  | $16.02\pm7.24$  |
| MYO   | Dice            | $0.84\pm0.014$  | $0.87\pm0.012$  | $0.87\pm0.013$  |
| MYO   | Hausdorff Dist. | $7.31\pm4.46$   | $6.07\pm3.66$   | $4.90\pm2.63$   |
| All   | Dice            | $0.82\pm0.020$  | $0.85\pm0.018$  | $0.86\pm0.018$  |
| All   | Hausdorff Dist. | $15.10\pm4.78$  | $13.73\pm4.44$  | $9.26\pm2.97$   |

This is the $95\%$ confidence interval of test performance. LV represents left ventricle, RV represents right ventricle, and MYO represents myocardium.