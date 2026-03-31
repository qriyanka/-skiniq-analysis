# skiniq — ai skincare analysis & product recommendation

computer vision pipeline that analyzes facial skin images, classifies 
skin type, scores key skin concerns, and recommends skincare products.

## what it does

- classifies skin as oily, dry, or normal using computer vision
- extracts 6 skin metrics per image using OpenCV
- trains a Random Forest classifier on extracted features
- recommends real skincare products based on detected skin type
- generates a full skin analysis report per image

## metrics analyzed

- texture score — laplacian variance of skin surface
- smoothness score — inverse texture measurement  
- pigmentation score — color channel variance across RGB
- redness score — red channel ratio analysis
- pore visibility — high frequency component detection
- overall health score — weighted combination of all metrics

## model performance

trained Random Forest classifier on 125 images across 3 skin types.
confusion matrix included in repo showing classification breakdown.

## pipeline

image → feature extraction (OpenCV) → skin type classification 
(Random Forest) → concern scoring → product recommendation (Sephora dataset)

## results

| skin type | avg smoothness | avg pigmentation | avg health |
|---|---|---|---|
| dry | 13.81 | 78.85 | 18.85 |
| normal | 17.57 | 84.11 | 19.00 |
| oily | 19.20 | 78.67 | 21.05 |

## tech stack

python · opencv · scikit-learn · pandas · matplotlib · seaborn · google colab

## datasets

- oily/dry/normal skin types image dataset — kaggle
- sephora cosmetics products dataset — kaggle

## built for

skin analysis pipelines used in beauty tech —
haut.ai · revieve · l'oréal tech · ulta beauty digital innovation
