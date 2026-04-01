## 1. glt clone DiffPROTACs and create the environment

```
git clone https://github.com/Fenglei104/DiffPROTACs.git
cd DiffPROTACs
conda env create -f env.yaml
conda activate DiffPROTACs
```


## 2. sample

We provide our preprocessed `protacs_test.pt` as the data file. Put it under `datasets/` and use the code like this in the command:

```
python test_ddp.py
```


  
