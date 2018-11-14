# Stage-wise Face Alignment using Global and Local Regressiors

This is a caffe-python implementation on Windows 10 for face alignment.

## Evaluation on 300w public test set
<center>

| Method | Common | Challenging | Full |
|:-------|:--------:|:-----:|:-------:|
| Stage(Projection) | 8.24 | 12.56 | 9.07 |
| Stage(Adjustment) | 6.25 | 10.16 | 7.02 |
| Stage(Global1) | 4.66 | 8.20 | 5.35 |
| Stage(Local1) | 3.45 | 6.49 | 4.05 |
| Stage(Global2) | 3.59 | 6.62 | 4.18 |
| Stage(Local2) | 3.29 | 6.14 | 3.85 |
| Stage(Global3) | 3.48 | 6.37 | 4.05 |
| Stage(Local3) | 3.28 | 6.09 | 3.83 |
|:-------|:--------:|:-----:|:-------:|
| Regression(Wild, simple net) | 4.07 | 6.90 | 4.62 |
| Regression(Wild, ResNet50) | 3.72 | 6.44 | 4.25 |
</center>

## Usage

### For training
1. Clone the repository
```
git clone https://github.com/hyunsungP/facelignmentregression
```

2. make data files (.h5)
make_wild_int.py, and so on.


3. training
On console window with caffe
```
caffe train --solver=models/ZF_solver1.prototxt --gpu=0
```

Other network are same.

### For Testing
```
test_300w_public.py
```

