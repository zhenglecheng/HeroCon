# 🌟 Contrastive Learning with Complex Heterogeneity

**Demo Code** for the paper  
📄 *"Contrastive Learning with Complex Heterogeneity"* — accepted at **KDD 2022**.

---

## ⚙️ Dependencies

Please make sure the following packages are installed before running the code:

- [PyTorch](https://pytorch.org/)
- [Pandas](https://pandas.pydata.org/)
- [OpenCV (cv2)](https://opencv.org/)
- [scikit-learn](https://scikit-learn.org/)

Install via:
```bash
pip install torch pandas opencv-python scikit-learn
```

---
## 📂 Dataset Preparation

You can download or prepare the datasets (Scene, XRMB, MNIST, CelebA) according to the configurations below.
Make sure the dataset folder structure follows the expected format in main.py.

* [MNIST](http://yann.lecun.com/exdb/mnist/): Handwritten digits for image classification
* [XRMB](https://home.ttic.edu/~klivescu/XRMB_data/full/README): Multi-modal speech dataset
* [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html): Multi-label facial recognition dataset
* [Scene](https://github.com/zhenglecheng/HeroCon/tree/main/data/scene):Multi-label scene classification dataset
---

## 🚀 Run the Demo

| **Setting** | **Dataset** | **Model** | **Command** |
|--------------|--------------|------------|--------------|
| Multi-view Multi-label | Scene | Linear | `python main.py -d scene -m linear -alpha 0.7 -beta 0.02 -e 200 -hid 100` |
| Multi-view Multi-class | XRMB | Linear | `python main.py -d xrmb -m linear -alpha 5 -beta 0.01 -e 300 -hid 100` |
| Multi-view Multi-class | MNIST | CNN | `python main.py -d mnist -m cnn -alpha 0.1 -beta 1 -e 300 -hid 200` |
| Multi-view Multi-label | CelebA | VGG | `python main.py -d celeba -m vgg -alpha 0.05 -beta 0.1 -e 300` |


---

## 🧠 Reference

If you use this code in your research, please cite:
```
@inproceedings{DBLP:conf/kdd/ZhengXZH22,
  author       = {Lecheng Zheng and
                  Jinjun Xiong and
                  Yada Zhu and
                  Jingrui He},
  editor       = {Aidong Zhang and
                  Huzefa Rangwala},
  title        = {Contrastive Learning with Complex Heterogeneity},
  booktitle    = {{KDD} '22: The 28th {ACM} {SIGKDD} Conference on Knowledge Discovery
                  and Data Mining, Washington, DC, USA, August 14 - 18, 2022},
  pages        = {2594--2604},
  publisher    = {{ACM}},
  year         = {2022}
}
```
