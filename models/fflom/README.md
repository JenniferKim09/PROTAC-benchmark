## 1. glt clone FFLOM and create the environment

- ```
git clone https://github.com/JenniferKim09/FFLOM.git
cd FFLOM
conda env create -f env.yaml -n fflom
conda activate fflom
  ```

## 2. download the prior models from [here](https://zenodo.org/record/7918738)


## 3. preprocess

We provide `data.txt` as the input file of FFLOM. Use the code like this (the save_fold can be changed) in the command:

- ```
python preprocess.py --data data.txt --save_fold ./data_preprocessed/test/ --name test --linker_design
  ```

## 4. sample

Use the code like this in the command:

- ```
python generate.py --path ./data_preprocessed/test/ --gen_out_path test_generation.txt --seed 66666666 --init_checkpoint ./good_ckpt/checkpoint306 --gen_num 250
  ```
  