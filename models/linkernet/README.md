## 1. glt clone LinkerNet and create the environment

- ```
git clone https://github.com/guanjq/LinkerNet.git
cd LinkerNet
conda create -n targetdiff python=3.8
conda activate targetdiff
conda install pytorch pytorch-cuda=11.6 -c pytorch -c nvidia
conda install pyg -c pyg
conda install rdkit openbabel tensorboard pyyaml easydict python-lmdb -c conda-forge
  ```

## 2. download the prior model (protac_model.pt) from [here](https://drive.google.com/drive/folders/1C1srELCCNJLk8v1smjvmbE-xYvnog5jU?usp=sharing)


## 3. sample

We provide `3d_index.pkl` as the input file of LinkerNet and `protac_all_gui.yml` as the config file. Put `3d_index.pkl` under `data/protac/` and use the code like this in the command:

- ```
python scripts/sample_protac.py protac_all_gui.yml --subset test --start_id 0 --end_id -1 --num_samples 250 --outdir outputs
  ```


  