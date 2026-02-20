# Benchmark for Activation Maximization techniques in the context of Hidden Semantics

## Dataset Requirements

- **Simple Sampling Method (SSM)**  
  Requires a dataset path structured as follows:

  ``
  path
  |---imagenet_test_small
  ``

  This folder should contain the test images used for top‑k sampling.

- **Activation Maximization (AM)**  
No dataset path is required, since AM generates synthetic inputs.

---

## Abstract

In recent years, growing concerns have emerged about the robustness and reliability of interpretability methods for understanding deep neural networks. Specifically, the reliability of visualization techniques—in particular Activation Maximization (AM)—has been called into question. This paper evaluates AM within the hidden semantics paradigm of interpretability by assessing its capacity to retrieve top semantics using ground‑truth comparisons. We implement three complementary metrics: transferability accuracy, CLIP similarity, and text similarity, applied in both automated and human evaluation (as equivalent metrics) settings. To emulate the behavior of hidden layers, we synthesize polysemantic neurons, as polysemanticity represents a distinctive feature of such layers. Our evaluation spans multiple architectures (AlexNet, VGG16, ResNet50, ViT) and a range of AM methods, from classical approaches (Simonyan, Yosinski, Olah) to recent advancements (MACO). Our findings indicate that dataset‑driven methods (SSM) consistently outperform synthetic AM techniques across both evaluation frameworks, although synthetic AM shows measurable improvement over time. These results offer new insights to guide the development of non‑linguistic interpretability methods.

---

## Dependencies

The experiments were conducted with the following package versions:

| Package              | Version   |
|----------------------|-----------|
| numpy                | 2.0.2     |
| timm                 | 1.0.24    |
| torch                | 2.10.0+cu128 |
| torchvision          | 0.25.0+cu128 |
| scipy                | 1.16.3    |
| matplotlib           | 3.10.0    |
| Pillow (PIL)         | 11.3.0    |
| tqdm                 | 4.67.3    |
| seaborn              | 0.13.2    |
| pandas               | 2.2.2     |
| transformers         | 5.0.0     |
| sentence-transformers| 5.2.3     |
| horama               | 0.3.0     |

---

## Notes

- Ensure that the dataset path for SSM is correctly set before running the notebook.  
- AM notebooks can be executed without any dataset preparation.  
- All comments and documentation are in English for clarity and reproducibility.
