# E4S - Colab Adaptation

This repository is a minimal adaptation of **E4S: Fine-Grained Face Swapping via Regional GAN Inversion** to run on **Google Colab**.

> 🔗 Original project: [https://github.com/Seasonly/E4S](https://github.com/Seasonly/E4S)

---

## 🚀 How to run it?

### 🔹 1. Open the notebook

Open [`e4s_swap_colab.ipynb`](e4s_swap_colab.ipynb) in **Google Colab**.

Run all the cells step by step until the last one to perform the face swap.

---

### 🔹 2. Upload your inputs

- Create a folder (e.g. `input/`)
- Put inside:
  - the **source image**
  - the **target image** or **video**

Update the input paths in the notebook accordingly.

---

### 🔹 3. Launch the inference

- Modify the config and weights paths if needed.
- Results will be saved in the `output/` folder by default.

---

## ⚠️ Important Notes

Run the following **before anything else** in a Colab cell:

```python
!pip install numpy==1.26
```

Then restart the Colab runtime (menu Runtime > Restart runtime) and re-run the notebook.

---

## 🧹 Optional: Cleanup after unzipping weights

If you unzip pretrained weights in `/content/workspace`, and want to move the files up and clean:

```bash
!unzip -q /content/workspace/e4s_model.zip -d /content/workspace/
!mv /content/workspace/e4s_model/* /content/workspace/
!rm -r /content/workspace/e4s_model
!rm /content/workspace/e4s_model.zip
```
Just change the path to the weights.
