## RAND

---

This repo is a Pytorch implementation of our NeurIPS 2023 paper: Adaptive Normalization for Non-stationary Time Series Forecasting: A Temporal Slice Perspective.

### Introduction

Time series data suffer from a non-stationary issue where the statistical properties or the distributions of the data vary rapidly over time. We further argue that the distribution is inconsistent across compact time slices and such inconsistency is not just on a per-instance basis. To alleviate the impact of such property, we propose a model-agnostic normalization framework named SAN. SAN models the non-stationarity in the fine-grained  temporal slices and explicitly learn to estimate future distributions, simplifying the the non-stationary forecasting task through divide and conquer.

![framework](figs/framework.png)

We conduct comparison experiments on **9 widely used datasets** with mainstream forecasting backbones, we also compare the performance of SAN and other plug-and-play non-stationary methods.

Multivariate forecasting results:

![multivariate](figs/multivariate.png)

Comparison with other plug-and-play non-stationary methods:

![compare](figs/compare.png)

### Usage

#### Environment and dataset setup

```bash
pip install -r requirements.txt
mkdir datasets
```

All the 9 datasets are available at the [Google Driver](https://drive.google.com/drive/folders/1ZOYpTUa82_jCcxIdTmyr0LXQfvaM9vIy) provided by Autoformer. Many thanks to their efforts and devotion!

#### Running

We provide ready-to-use scripts for RAND enhanced backbone models.

```bash
sh run_rand.sh
```



### Citation

If you find this repository useful for your work, please consider citing it as follows:

```bibtex
@inproceedings{liu2023adaptive,
  title={Adaptive Normalization for Non-stationary Time Series Forecasting: A Temporal Slice Perspective},
  author={Liu, Zhiding and Cheng, Mingyue and Li, Zhi and Huang, Zhenya and Liu, Qi and Xie, Yanhu and Chen, Enhong},
  booktitle={Thirty-seventh Conference on Neural Information Processing Systems},
  year={2023}
}
```

