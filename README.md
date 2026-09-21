# Agent-Image-DescriptionAndClassifier

A Jupyter/Colab notebook with two Gradio-powered image AI demos:

1. **Image Captioning** — Uses Salesforce's [BLIP](https://huggingface.co/Salesforce/blip-image-captioning-base) model (via Hugging Face `transformers`) to generate a natural-language caption for an uploaded image.
2. **Image Classification** — Uses a pretrained `torchvision` ResNet-18 (ImageNet weights) to classify an uploaded image and return the top-3 predicted labels with confidence scores.

Each demo launches its own Gradio web interface for uploading an image and viewing the result.

## Notebook

- [`Untitled27.ipynb`](Untitled27.ipynb)

## Requirements

```bash
pip install gradio transformers torch torchvision requests
```

## Usage

Open the notebook in Jupyter or Google Colab and run the cells in order:

1. Load the BLIP processor/model and launch the captioning interface.
2. Load ResNet-18, download ImageNet class labels, and launch the classification interface.

Each `iface.launch()` call starts a local Gradio server (and a temporary public share link when run in a hosted/Colab environment).
