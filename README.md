# Long-Tailed-Classification-Leaderboard
date: 2021/3/3（Updated 2021/3/3）
auther: YW YSZ

## 1. Introduction

List of abbreviations:
Abbreviations   | ReW | TrL | MeL   | DeL | Aug     |SeSu | OtM 
:----: | :----: | :--: | :------:   | :---:    | :---:   | :---:    | :--: 
Full names | Re-weighting | Transfer Learning | Meta Learning   | Decoupling Learning    | Data Augmentation   | Self-Supervised Learning    | Other methods 



## 2. Benchmark datasets

Dataset   | Year | Images(Triain/Val/Test) | Classes   | Max images | Min images     |Imbalance factor  | Reported by 
:-----: | :----: | :--: | :------:   | :---:    | :---:   | :---:    | :--: 
[CIFAR-LT-10](https://arxiv.org/abs/1901.05555) | 2019 | 50000–11203/--/10000 | 10   | 5,000    | 500–25   | 1.0–200.0    | [Source](https://arxiv.org/abs/2003.10780) 
[CIFAR-LT-100](https://arxiv.org/abs/1901.05555) | 2019 | 50000–9502/--/10000 | 100   | 500    | 500–2   | 1.0–200.0    | [Source](https://arxiv.org/abs/2003.10780) 
[ImageNet-LT](https://arxiv.org/abs/1904.05160) | 2019 | 115846/20000/50000 | 1000   | 1280    | 5   | 256.0    | [Source](https://arxiv.org/abs/2003.10780) 
[Places-LT](https://arxiv.org/abs/1904.05160) | 2019 | 62500/7300/36500 | 365   | 4980    | 5   | 996.0    | [Source](https://arxiv.org/abs/2003.10780) 
[iNat 2017](https://github.com/visipedia/inat_comp/tree/master/2017) | 2017 | 579184/95986/-- | 5089   | 3919    | 9   | 435.4    | [Source](https://arxiv.org/abs/2003.10780) 
[iNat 2018](https://github.com/visipedia/inat_comp/tree/master/2018) | 2018 | 437513/24426/-- | 8142   | 1000    | 2   | 500.0    | [Source](https://arxiv.org/abs/2003.10780) 




## 3. Leaderboard
### 3.1 CIFAR-10-LT

Evaluation metric: classification **error** rate.

``IF`` represents ``Imbalance factor``.

#####Backbone: ResNet-32

|                            Method                            |     Venue     | Year | Backbone  |  Type   | IF=10 | IF=50 | IF=100 | Code  |                         Reported by                          |
| :----------------------------------------------------------: | :-----------: | :--: | --------- | :-----: | :---: | :---: | :----: | :---: | :----------------------------------------------------------: |
|   [Class-Balanced Loss](https://arxiv.org/abs/1901.05555)    |     CVPR      | 2019 | ResNet-32 |   ReW   | 12.51 | 20.73 | 25.43  | ----  |          [Source](https://arxiv.org/abs/1901.05555)          |
|         [LDAM-DRW](https://arxiv.org/abs/1906.07413)         |    NeurIPS    | 2019 | ResNet-32 |   ReW   | 11.84 | ----- | 22.97  | ----  |          [Source](https://arxiv.org/abs/1906.07413)          |
|          [MW-Net](https://arxiv.org/abs/1902.07379)          |    NeurIPS    | 2019 | ResNet-32 | ReW/MeL | 12.16 | 19.94 | 24.79  | ----  |          [Source](https://arxiv.org/abs/1902.07379)          |
|         [LDAM-M2m](https://arxiv.org/abs/2004.00431)         |     CVPR      | 2020 | ResNet-32 |   TrL   | 12.5  | ----- |  20.9  | ----- |          [Source](https://arxiv.org/abs/2004.00431)          |
|           [BBN](https://arxiv.org/abs/1912.02413)            |     CVPR      | 2020 | ResNet-32 |   DeL   | 11.68 | 17.82 | 20.18  | ----  |          [Source](https://arxiv.org/abs/1912.02413)          |
|       [CBasDA-LDAM](https://arxiv.org/abs/2003.10780)        |     CVPR      | 2020 | ResNet-32 |   ReW   | 12.6  | 17.77 | 22.77  | ----  |          [Source](https://arxiv.org/abs/2003.10780)          |
|     [Balanced Softmax](https://arxiv.org/abs/2008.11037)     | ECCV-Workshop | 2020 | ResNet-32 |   OtM   |  9.1  | ----- |  16.9  | ----  |          [Source](https://arxiv.org/abs/2008.11037)          |
|     [De-confound-TDE](https://arxiv.org/abs/2009.12991)      |    NeurIPS    | 2020 | ResNet-32 |   OtM   | 11.5  | 16.4  |  19.4  | ----  |          [Source](https://arxiv.org/abs/2009.12991)          |
|          [BALMS](https://arxiv.org/abs/2007.10740)           |    NeurIPS    | 2020 | ResNet-32 |   ReW   |  8.7  | ----- |  15.1  | ----  |          [Source](https://arxiv.org/abs/2007.10740)          |
|      [LDAM-DRW + SSP](https://arxiv.org/abs/2006.07529)      |    NeurIPS    | 2020 | ResNet-32 |  SeSu   | 11.47 | 17.87 | 22.17  | ----  |          [Source](https://arxiv.org/abs/2006.07529)          |
| [Baseline + tricks](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |     AAAI      | 2021 | ResNet-32 |   OtM   | ----- | 16.41 | 19.97  | ----  | [Source](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |
|        [Remix-DRW](https://arxiv.org/abs/2007.03943)         | ECCV-Workshop | 2020 | ResNet-32 |   Aug   | 10.98 | ----- | 20.24  | ----  |          [Source](https://arxiv.org/abs/2007.03943)          |

#####Backbone: ResNet-18

|                 Method                  | Venue | Year | Backbone  | Type | IF=10 | IF=50 | IF=100 | Code |                Reported by                 |
| :-------------------------------------: | :---: | :--: | --------- | :--: | :---: | :---: | :----: | :--: | :----------------------------------------: |
| [FSA](https://arxiv.org/abs/2008.03673) | ECCV  | 2020 | ResNet-18 | Aug  | 8.25  | 15.29 | 19.43  | ---- | [Source](https://arxiv.org/abs/2008.03673) |

#####Backbone: ResNet-34

Method   | Venue | Year | Backbone   | Type | IF=10     | IF=50 | IF=100    | Code | Reported by 
:-----: | :----: | :--: | --------   | :---:    | :---:   | :---:    | :--: | :--: | :--:
[FSA](https://arxiv.org/abs/2008.03673) | ECCV | 2020 | ResNet-34   | Aug    | 8.8   | 15.51    | 17.94 | ---- | [Source](https://arxiv.org/abs/2008.03673) 


### 3.2 CIFAR-100- LT

Evaluation metric: classification **error** rate.

##### Backbone: ResNet-32

|                            Method                            |     Venue     | Year | Backbone  |  Type   | IF=10 | IF=50 | IF=100 | Code  |                         Reported by                          |
| :----------------------------------------------------------: | :-----------: | :--: | :-------: | :-----: | :---: | :---: | :----: | :---: | :----------------------------------------------------------: |
|   [Class-Balanced Loss](https://arxiv.org/abs/1901.05555)    |     CVPR      | 2019 | ResNet-32 |   ReW   | 42.01 | 54.68 | 60.40  | ----  |          [Source](https://arxiv.org/abs/1901.05555)          |
|         [LDAM-DRW](https://arxiv.org/abs/1906.07413)         |    NeurIPS    | 2019 | ResNet-32 |   ReW   | 41.29 | ----- | 57.96  | ----  |          [Source](https://arxiv.org/abs/1906.07413)          |
|          [MW-Net](https://arxiv.org/abs/1902.07379)          |    NeurIPS    | 2019 | ResNet-32 | ReW/MeL | 41.54 | 53.26 | 57.91  | ----  |          [Source](https://arxiv.org/abs/1902.07379)          |
|         [LDAM-M2m](https://arxiv.org/abs/2004.00431)         |     CVPR      | 2020 | ResNet-32 |   TrL   | 42.4  | ----- |  56.5  | ----- |          [Source](https://arxiv.org/abs/2004.00431)          |
|           [BBN](https://arxiv.org/abs/1912.02413)            |     CVPR      | 2020 | ResNet-32 |   DeL   | 40.88 | 52.98 | 57.44  | ----  |          [Source](https://arxiv.org/abs/1912.02413)          |
|       [CBasDA-LDAM](https://arxiv.org/abs/2003.10780)        |     CVPR      | 2020 | ResNet-32 |   ReW   | 42.0  | 50.84 | 60.47  | ----  |          [Source](https://arxiv.org/abs/2003.10780)          |
|        [LFME+LDAM](https://arxiv.org/abs/2001.01536)         |     ECCV      | 2020 | ResNet-32 |   TrL   | ----- | ----- |  56.2  | ----  |          [Source](https://arxiv.org/abs/2001.01536)          |
|     [Balanced Softmax](https://arxiv.org/abs/2008.11037)     | ECCV-Workshop | 2020 | ResNet-32 |   OtM   | 36.9  | ----- |  49.7  | ----  |          [Source](https://arxiv.org/abs/2008.11037)          |
|     [De-confound-TDE](https://arxiv.org/abs/2009.12991)      |    NeurIPS    | 2020 | ResNet-32 |   OtM   | 40.4  | 49.7  |  55.9  | ----  |          [Source](https://arxiv.org/abs/2009.12991)          |
|          [BALMS](https://arxiv.org/abs/2007.10740)           |    NeurIPS    | 2020 | ResNet-32 |   ReW   | 37.0  | ----- |  49.2  | ----  |          [Source](https://arxiv.org/abs/2007.10740)          |
|      [LDAM-DRW + SSP](https://arxiv.org/abs/2006.07529)      |    NeurIPS    | 2020 | ResNet-32 |  SeSu   | 41.09 | 52.89 | 56.57  | ----  |          [Source](https://arxiv.org/abs/2006.07529)          |
| [Baseline + tricks](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |     AAAI      | 2021 | ResNet-32 |   OtM   | ----- | 48.31 | 52.17  | ----  | [Source](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |
|        [Remix-DRW](https://arxiv.org/abs/2007.03943)         | ECCV-Workshop | 2020 | ResNet-32 |   Aug   | 38.77 | ----- | 53.23  | ----  |          [Source](https://arxiv.org/abs/2007.03943)          |

##### Backbone: ResNet-18

|                 Method                  | Venue | Year | Backbone  | Type | IF=10 | IF=50 | IF=100 | Code |                Reported by                 |
| :-------------------------------------: | :---: | :--: | :-------: | :--: | :---: | :---: | :----: | :--: | :----------------------------------------: |
| [FSA](https://arxiv.org/abs/2008.03673) | ECCV  | 2020 | ResNet-18 | Aug  | 34.92 | 48.1  | 53.43  | ---- | [Source](https://arxiv.org/abs/2008.03673) |

##### Backbone: ResNet-34

Method   | Venue | Year | Backbone   | Type | IF=10     | IF=50 | IF=100    | Code | Reported by 
:-----: | :----: | :--: | :------:   | :---:    | :---:   | :---:    | :--: | :--: | :--:
[FSA](https://arxiv.org/abs/2008.03673) | ECCV | 2020 | ResNet-34   | Aug    | 34.71   | 47.83    | 51.49 | ---- | [Source](https://arxiv.org/abs/2008.03673) 

### 3.3 ImageNet-LT

Evaluation metric: closed-set setting/Top-1 classification **accuracy**.

#####Backbone: ResNet-10

|                            Method                            |  Venue  | Year | Backbone  | Type | Many-Shot | Medium-Shot | Few-Shot |  ALL  | Code | Reported by                                                  |
| :----------------------------------------------------------: | :-----: | :--: | :-------: | :--: | :-------: | :---------: | :------: | :---: | :--: | ------------------------------------------------------------ |
|           [OLTR](https://arxiv.org/abs/1904.05160)           |  CVPR   | 2019 | ResNet-10 | TrL  |   43.2    |    35.1     |   18.5   | 35.6  | ---- | [Source](https://arxiv.org/abs/1904.05160)                   |
|           [LWS](https://arxiv.org/abs/1910.09217)            |  ICLR   | 2020 | ResNet-10 | DeL  |   -----   |    -----    |   ----   | 41.4  | ---- | [Source](https://arxiv.org/abs/1910.09217)                   |
| [IEM](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html) |  CVPR   | 2020 | ResNet-10 | OtM  |   48.9    |    44.0     |   24.4   | 43.2  | ---- | [Source](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html) |
|        [LFME+OLTR](https://arxiv.org/abs/2001.01536)         |  ECCV   | 2020 | ResNet-10 | TrL  |   47.0    |    37.9     |   19.2   | 38.8  | ---- | [Source](https://arxiv.org/abs/2001.01536)                   |
|           [FSA](https://arxiv.org/abs/2008.03673)            |  ECCV   | 2020 | ResNet-10 | Aug  |   47.3    |    31.6     |   14.7   | 35.2  | ---- | [Source](https://arxiv.org/abs/2008.03673)                   |
|          [BALMS](https://arxiv.org/abs/2007.10740)           | NeurIPS | 2020 | ResNet-10 | ReW  |   50.3    |    39.5     |   25.3   | 41.8  | ---- | [Source](https://arxiv.org/abs/2007.10740)                   |
|        [cRT + SSP](https://arxiv.org/abs/2006.07529)         | NeurIPS | 2020 | ResNet-10 | SeSu |   -----   |    -----    |   ----   | 43.2  | ---- | [Source](https://arxiv.org/abs/2006.07529)                   |
| [Baseline + tricks](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |  AAAI   | 2021 | ResNet-10 | OtM  |   -----   |    -----    |   ----   | 43.31 | ---- | [Source](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |

#####Backbone: ResNeXt-50

|                 Method                  | Venue | Year |  Backbone  | Type | Many-Shot | Medium-Shot | Few-Shot | ALL  | Code | Reported by                                |
| :-------------------------------------: | :---: | :--: | :--------: | :--: | :-------: | :---------: | :------: | :--: | :--: | ------------------------------------------ |
| [LWS](https://arxiv.org/abs/1910.09217) | ICLR  | 2020 | ResNeXt-50 | DeL  |   60.2    |    47.2     |   30.3   | 49.9 | ---- | [Source](https://arxiv.org/abs/1910.09217) |

#####Backbone: ResNeXt-152

Method   | Venue | Year | Backbone   | Type  | Many-Shot     | Medium-Shot | Few-Shot | ALL |Code | Reported by 
:-----: | :----: | :--: | :------:   | :---:    | :---:   | :---:    | :--: | :--: | :--: | ----
[LWS](https://arxiv.org/abs/1910.09217) | ICLR | 2020 | ResNeXt-152   | DeL    | 63.5   | 50.4    | 34.2 | 53.3 | ---- | [Source](https://arxiv.org/abs/1910.09217) 

### 3.4 Places-LT

Evaluation metric: closed-set setting/Top-1 classification **accuracy**.

##### Backbone: ResNet-152

Method   | Venue | Year | Backbone | Type  | Many-Shot     | Medium-Shot | Few-Shot | ALL |Code | Reported by 
:-----: | :----: | :--: | :---:    | :---:   | :---:    | :--: | :--: | :--: | ---- | :--: 
[OLTR](https://arxiv.org/abs/1904.05160) | CVPR | 2019 | ResNet-152 | TrL    | 44.7   | 37    | 25.3 | 35.9 | ---- | [Source](https://arxiv.org/abs/1904.05160) 
[LWS](https://arxiv.org/abs/1910.09217) | ICLR | 2020 | ResNet-152 | DeL    | 40.6   | 39.1    | 28.6 | 37.6 | ---- | [Source](https://arxiv.org/abs/1910.09217) 
[τ -normalized](https://arxiv.org/abs/1910.09217) | ICLR | 2020 | ResNet-152 | DeL    | 37.8   | 40.7    | 31.8 | 37.9 | ---- | [Source](https://arxiv.org/abs/1910.09217) 
[IEM](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html)  | CVPR  | 2020  | ResNet-152 | OtM    | 46.8   | 39.2    | 28.0 |  39.7 | ---- | [Source](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html)
[LFME+OLTR](https://arxiv.org/abs/2001.01536)| ECCV | 2020 | ResNet-152 | TrL    | 39.3   | 39.6    | 24.2 | 36.2 | ---- | [Source](https://arxiv.org/abs/2001.01536)
[FSA](https://arxiv.org/abs/2008.03673)  | ECCV | 2020 | ResNet-152 | Aug    | 42.8  | 37.5    | 22.7| 36.4| ---- | [Source](https://arxiv.org/abs/2008.03673)

##### Backbone: ResNet-10

|                  Method                   |  Venue  | Year | Backbone  | Type | Many-Shot | Medium-Shot | Few-Shot | ALL  | Code | Reported by |
| :---------------------------------------: | :-----: | :--: | :-------: | :--: | :-------: | :---------: | :------: | :--: | :--: | ----------- |
| [BALMS](https://arxiv.org/abs/2007.10740) | NeurIPS | 2020 | ResNet-10 | ReW  |   41.2    |    39.8     |   31.6   | 38.7 | ---- |             |

### 3.5 iNaturalist 

Evaluation metric: Top-1 classification **accuracy**

#####Backbone: ResNet-50

|                            Method                            |     Venue     | Year | Backbone  | Type | iNat-2017(Top1) |  iNat-2018(Top1)   | Code |                         Reported by                          |
| :----------------------------------------------------------: | :-----------: | :--: | :-------: | :--: | :-------------: | :----------------: | :--: | :----------------------------------------------------------: |
|         [CB Focal](https://arxiv.org/abs/1901.05555)         |     CVPR      | 2019 | ResNet-50 | ReW  |      58.08      |       61.12        | ---- |          [Source](https://arxiv.org/abs/1901.05555)          |
|           [LWS](https://arxiv.org/abs/1910.09217)            |     ICLR      | 2020 | ResNet-50 | DeL  |      -----      | 65.9/69.5 (90/200) | ---- |          [Source](https://arxiv.org/abs/1910.09217)          |
| [IEM](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html) |     CVPR      | 2020 | ResNet-50 | OtM  |      -----      |        70.2        | ---- | [Source](https://openaccess.thecvf.com/content_CVPR_2020/html/Zhu_Inflated_Episodic_Memory_With_Region_Self-Attention_for_Long-Tailed_Visual_Recognition_CVPR_2020_paper.html) |
|           [BBN](https://arxiv.org/abs/1912.02413)            |     CVPR      | 2020 | ResNet-50 | DeL  |      63.39      |       66.29        | ---- |          [Source](https://arxiv.org/abs/1912.02413)          |
|         [BBN(2×)](https://arxiv.org/abs/1912.02413)          |     CVPR      | 2020 | ResNet-50 | DeL  |      65.75      |       69.62        | ---- |          [Source](https://arxiv.org/abs/1912.02413)          |
|        [CBasDA-CE](https://arxiv.org/abs/2003.10780)         |     CVPR      | 2020 | ResNet-50 | ReW  |      59.38      |       67.55        | ---- |          [Source](https://arxiv.org/abs/2003.10780)          |
|           [FSA](https://arxiv.org/abs/2008.03673)            |     ECCV      | 2020 | ResNet-50 | Aug  |      61.96      |       65.91        | ---- |          [Source](https://arxiv.org/abs/2008.03673)          |
|        [cRT + SSP](https://arxiv.org/abs/2006.07529)         |    NeurIPS    | 2020 | ResNet-50 | SeSu |      -----      |        68.1        | ---- |          [Source](https://arxiv.org/abs/2006.07529)          |
| [Baseline + tricks](https://cs.nju.edu.cn/wujx/paper/AAAI2021_Tricks.pdf) |     AAAI      | 2021 | ResNet-50 | OtM  |      -----      |       70.87        | ---- |          [Source](https://arxiv.org/abs/2007.10740)          |
|        [Remix-DRS](https://arxiv.org/abs/2007.03943)         | ECCV-Workshop | 2020 | ResNet-50 | Aug  |      -----      |       70.74        | ---- |          [Source](https://arxiv.org/abs/2007.03943)          |

#####Backbone: ResNet-152

Method   | Venue | Year | Backbone   |Type  | iNat-2017(Top1)  | iNat-2018(Top1)  | Code | Reported by 
:-----: | :----: | :--: | :------:   | :---:   | :---:    | :--:  | :--:  | :--: 
[CB Focal](https://arxiv.org/abs/1901.05555)  | CVPR | 2019 | ResNet-152   | ReW    | 61.84 | 64.16 | ---- |  [Source](https://arxiv.org/abs/1901.05555)
[LWS](https://arxiv.org/abs/1910.09217) | ICLR | 2020 | ResNet-152   | DeL   | -----    | 69.1/72.1 (90/200)  |----   | [Source](https://arxiv.org/abs/1910.09217) 
[FSA](https://arxiv.org/abs/2008.03673) | ECCV | 2020 | ResNet-152   | Aug   | 66.58    | 69.08  | ----  | [Source](https://arxiv.org/abs/2008.03673) 

## 4. Contact
Yan Wang : yanwang@smail.nju.edu.cn 

Yongshun Zhang: zhangys@lamda.nju.edu.cn


## 5. References
- Cui et.al., Class-Balanced Loss Based on Effective Number of Samples, CVPR 2019. 
- Shu et.al., Meta-Weight-Net: Learning an Explicit Mapping For Sample Weighting, NeurIPS 2019.
- Cao et.al., Learning Imbalanced Datasets with Label-Distribution-Aware Margin Loss, NeurIPS 2019.
- Kang et.al., Decoupling Representation and Classifier for Long-Tailed Recognition, ICLR 2020.
- Kim et.al., M2m: Imbalanced Classification via Major-to-minor Translation, CVPR 2020.
- Zhou et.al., BBN: Bilateral-Branch Network with Cumulative Learning for Long-Tailed Visual Recognition, CVPR 2020.
- Tang et.al., Long-Tailed Classification by Keeping the Good and Removing the Bad Momentum Causal Effect, NeurIPS 2020.
- Zhu et.al., Inflated Episodic Memory with Region Self-Attention for Long-Tailed Visual Recognition, CVPR 2020.
- Yang et.al., Rethinking the Value of Labels for Improving Class-Imbalanced Learning, NeurIPS 2020.
- Liu et.al., Large-Scale Long-Tailed Recognition in an Open World, CVPR 2019.
- Ren et.al., Balanced Meta-Softmax for Long-Tailed Visual Recognition, NeurIPS 2020.
- Jamal et.al., Rethinking Class-Balanced Methods for Long-Tailed Visual Recognition from a Domain Adaptation Perspective, CVPR 2020.
- Xiang et.al., Learning From Multiple Experts: Self-paced Knowledge Distillation for Long-tailed Classification, ECCV 2020.
- Chu et.al., Feature Space Augmentation for Long-Tailed Data, ECCV 2020.
- Ren et.al., Balanced Activation for Long-tailed Visual Recognition, ECCV 2020.
- Zhang et.al., Bag of Tricks for Long-Tailed Visual Recognition with Deep Convolutional Neural Networks, AAAI 2021.
- Chou et.al., Remix: Rebalanced Mixup, ECCV'2020 Workshop.
