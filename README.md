# MambaHSI: Spatial-Spectral Mamba for Hyperspectral Image Classification


## 🚀 Getting Started

### Installation

```sh
conda create -n MambaHSI_env python=3.9
conda activate MambaHSI_env
conda install pytorch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 pytorch-cuda=11.7 -c pytorch -c nvidia
pip install packaging==24.0
pip install triton==2.2.0
pip install mamba-ssm==1.2.0
pip install spectral
pip install scikit-learn==1.4.1.post1
```

### Data Preparation
The dataset can download [Google Drive](https://drive.google.com/file/d/1d-fzMXYhpwis9o_x8hPz4uHx0z5tg7LD/view?usp=sharing) and [BaiduNetdisk](https://pan.baidu.com/s/1SqzP-Y6mbuR1PRz9uGGp1Q?pwd=8ne2).

```
data
└── UP/
    ├── PaviaU.mat 
    └── PaviaU_gt.mat
    ...
└── Houston/
    ├── Houston.mat 
    └── Houston_GT.mat
    ...
└── HanChuan/
    ├── WHU_Hi_HanChuan.mat 
    └── WHU_Hi_HanChuan_gt.mat
    ...
└── HongHu/  
    ├── WHU_Hi_HongHu.npy
    └── WHU_Hi_HongHu_gt.npy
```



**Training:**
```
python train_MambaHSI.py --dataset_index 0
python train_MambaHSI.py --dataset_index 1
python train_MambaHSI.py --dataset_index 2
python train_MambaHSI.py --dataset_index 3
```

## Citation	

If you use our work in your research, please cite: 

```
@ARTICLE{MambaHSI_TGRS24,
  author={Li, Yapeng and Luo, Yong and Zhang, Lefei and Wang, Zengmao and Du, Bo},
  journal={IEEE Transactions on Geoscience and Remote Sensing}, 
  title={MambaHSI: Spatial-Spectral Mamba for Hyperspectral Image Classification}, 
  year={2024},
  volume={62},
  number={},
  pages={1-16},
  keywords={Hyperspectral Image Classification; Mamba; State Space Models; Transformer},
  }
```

## Acknowledgement
Part of our MambaHSI framework is referred to [CVSSN](https://github.com/lms-07/CVSSN.git) and [SSFCN](https://github.com/YonghaoXu/SSFCN.git). We thank all the contributors for open-sourcing.