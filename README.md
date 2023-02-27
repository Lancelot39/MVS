## Enhancing Multi-View Smoothness for Sequential Recommendation Models

This repository contains the code for our TOIS paper ***Enhancing Multi-View Smoothness for Sequential Recommendation Models***.

## Overview

We propose ***MVS***, a general training framework for enhancing the multi-view smoothness of sequential recommendation models using implicit feedback data. In our approach, we leverage a complementary model and devise three regularizers to guarantee label smoothness, context smoothness and model smoothness. *In this project, we mainly release the implemented code on the SASRec model*.

![](figure/model.png)

## Train DCLR

In the following section, we describe how to train a DCLR model by using our code.

### Environment

To faithfully reproduce our results, please follow the same environment as in our previous project [S3-Rec](https://github.com/RUCAIBox/CIKM2020-S3Rec)

### Data

We also utilize the released data from [S3-Rec](https://github.com/RUCAIBox/CIKM2020-S3Rec)

### Training scripts

In our approach, we first train a complementary model (e.g., SASRec), and then utilize it to help train our target model.
```bash
cd code
python run_base_sample.py --data_name Beauty
python run_mvs_sample.py --data_name Beauty
```

We also provide the code under the full-sort ranking setting:
```bash
cd code
python run_base_full.py --data_name Beauty
python run_mvs_full.py --data_name Beauty
```

## Citation

Please cite our paper if you use MVS in your work:

```bibtex
@article{zhou2023mvs,
   title={Enhancing Multi-View Smoothness for Sequential Recommendation Models},
   author={Zhou, Kun and Wang, Hui and Wen, Ji-Rong and Zhao, Xin},
   booktitle = {{TOIS}},
   year={2023}
}
```
