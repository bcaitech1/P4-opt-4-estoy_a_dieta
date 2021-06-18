# Model Customize : Pruning & decomposition

||MACs|F1|Competition Score|
|------|---|---|----|
|Before|1688940.0|0.6206|0.4005|
|After|1083210.0|0.6149|0.3431|

## Envrionment
```
pytorch '1.7.1+cu101'
albumentations
sklearn
ptflops
```

# Test_Demo
### Before
```python
python test_demo.py --customized_model False --eval True
```
### After
```python
python test_demo.py --customized_model True --eval True
```

## Directory
```
Model Customize/
├──input/
|  └── data/
|      ├── train/
|          ├── trainImg00001.jpg
|          ├── ...
|          └── trainImg22640.jpg
|      └── val/
|          ├── valImg0001.jpg
|          ├── ...
|          └── valImg8816.jpg
├──pretrained/
│  ├── ShuffleNet_final.pt
│  └── shufflenet_g3_wd4.pth
├── dataloader.py
├── ...
├── test_demo.py
└── utils.py
```
