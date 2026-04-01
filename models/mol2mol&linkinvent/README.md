## 1. glt clone REINVENT4 and create the environment

- ```
git clone git@github.com:MolecularAI/REINVENT4.git
cd REINVENT4
conda create --name reinvent4 python=3.10
conda activate reinvent4
python install.py cu126
  ```

## 2. download the prior models from [here](https://zenodo.org/records/15641297)


## 3. LINK-INVENT

We provide `sampling_linkinvent.toml` for the sampling of LINK-INVENT, and only the `smiles_file` (line 17) and `output_file` (line 19) need to be changed during usage. All input smiles_files of our 40 targets are provided in `data_mol2mol&linkinvent.zip`. Use the code like this in the command:

- ```
reinvent -l test.log /your/path/to/sampling_linkinvent.toml
  ```

## 4. mol2mol

We provide `sampling_mol2mol.toml` for the sampling of mol2mol, and only the `smiles_file` (line 17) and `output_file` (line 22) need to be changed during usage. All input smiles_files of our 40 targets are provided in `data_mol2mol&linkinvent.zip`. Use the code like this in the command:

- ```
reinvent -l test.log /your/path/to/sampling_mol2mol.toml
  ```
  