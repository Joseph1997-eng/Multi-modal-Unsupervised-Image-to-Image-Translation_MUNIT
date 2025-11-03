# Multi-modal Unsupervised Image-to-Image Translation (MUNIT)

This repository contains an implementation of the **MUNIT** framework, as described in the ECCV 2018 paper: "[Multimodal Unsupervised Image-to-Image Translation](https://arxiv.org/abs/1804.04732)".

This project is implemented in the Jupyter Notebook `C3W3_MUNIT_(Optional).ipynb`.

---

## Introduction

Unsupervised image-to-image translation aims to learn a mapping between two different image domains (e.g., cats to dogs, summer to winter) without corresponding image pairs.

While many methods learn a single, deterministic mapping, the **MUNIT** framework is designed to learn a *multimodal* mapping. This means that for a single input image, the model can generate multiple, diverse, and realistic translations.


### Core Concept

The MUNIT framework is based on the assumption that an image's representation can be decomposed into two parts:

1.  **Content Code:** A domain-invariant code that represents the underlying structure and content of the image (e.g., the pose of an animal).
2.  **Style Code:** A domain-specific code that captures the appearance and stylistic features (e.g., the animal's fur color and texture).

To translate an image from domain A to domain B, the model:
1.  Encodes the source image (domain A) to extract its **content code**.
2.  Samples a random **style code** from the style space of the target domain (domain B).
3.  Combines the source content code and the target style code using a decoder to generate the final, translated image.

By sampling different style codes, the model can produce a wide variety of outputs from a single input image.

---

## About this Repository

This repository provides a hands-on implementation of the MUNIT framework within a Jupyter Notebook. It appears to be an exercise from an educational course (e.g., "Course 3, Week 3").

The primary file is:
* `C3W3_MUNIT_(Optional).ipynb`: A self-contained notebook that walks through the MUNIT architecture, loss functions, and training process.

---

## Usage

To get started with this project, you will need to have Python, Jupyter, and standard deep learning libraries (like PyTorch or TensorFlow) installed.

### 1. Clone the Repository

```bash
git clone [https://github.com/Joseph1997-eng/Multi-modal-Unsupervised-Image-to-Image-Translation_MUNIT.git](https://github.com/Joseph1997-eng/Multi-modal-Unsupervised-Image-to-Image-Translation_MUNIT.git)
cd Multi-modal-Unsupervised-Image-to-Image-Translation_MUNIT
```

### 2. Install Dependencies

Install the required libraries. The exact dependencies will be listed within the Jupyter Notebook. A typical setup might include:

```bash
pip install torch torchvision numpy matplotlib jupyter
```

### 3. Run the Notebook

Launch Jupyter Notebook and open the main file:

```bash
jupyter notebook C3W3_MUNIT_(Optional).ipynb
```

Follow the instructions within the notebook to load data, build the MUNIT model, and run the training and translation experiments.

---

## Acknowledgments & Original Paper

This code is an implementation based on the original MUNIT paper. All credit for the model architecture and core concepts goes to the original authors.

* **Paper:** [Multimodal Unsupervised Image-to-Image Translation](https://arxiv.org/abs/1804.04732) (ECCV 2018)
* **Authors:** Xun Huang, Ming-Yu Liu, Serge Belongie, Jan Kautz
* **Official NVIDIA Repository:** [https://github.com/NVlabs/MUNIT](https://github.com/NVlabs/MUNIT)

---

## License

This project is licensed under the [MIT License](LICENSE).
