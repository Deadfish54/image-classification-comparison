# Image Classification: MobileNetV2 vs ViT vs CLIP

Compares three pretrained image classifiers on ImageNet validation images: a lightweight CNN (MobileNetV2), a Vision Transformer (ViT), and zero-shot CLIP. Measures accuracy, confidence calibration and inference speed.

## Results (200 ImageNet-mini validation images)

| Model | Accuracy | Avg confidence | Avg time / image | Images / sec |
|---|---|---|---|---|
| ViT | **80.5%** | 83.1% | 11.3 ms | 88.8 |
| MobileNetV2 | 66.5% | 61.2% | 95.1 ms | 10.5 |
| CLIP (zero-shot) | 56.5% | 54.1% | **9.2 ms** | **108.8** |

- All three models agreed and were correct on 43% of images.
- ViT was the only correct model on 13 images, CLIP on 6, MobileNetV2 on 2.
- Every model is noticeably less confident when wrong, with ViT showing the clearest gap (89.4% vs 57.1%).

## Notebooks

| Notebook | Contents |
|---|---|
| `01_mobilenetv2_classification.ipynb` | MobileNetV2 predictions on the sample |
| `02_vit_classification.ipynb` | ViT predictions and top-3 outputs |
| `03_clip_zeroshot.ipynb` | CLIP zero-shot classification with ImageNet label prompts |
| `04_comparison.ipynb` | Side-by-side comparison, agreement analysis, confidence and speed |

## Running

Run on Kaggle with the `imagenetmini-1000` dataset attached. Uses TensorFlow/Keras (MobileNetV2) and Hugging Face Transformers (ViT, CLIP).

**Author:** Mahbubul Alam, East Delta University
