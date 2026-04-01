## 1. glt clone ShapeLinker and create the environments

Two environments are needed for this model. 

- ```
git clone https://github.com/aivant/ShapeLinker
cd ShapeLinker
conda env create -f env.yaml
conda install -c conda-forge mamba
mamba create -n shape_align python=3.9 pytorch=1.13.0 torchvision pytorch-cuda=11.6 fvcore iopath nvidiacub pytorch3d -c bottler -c fvcore -c iopath -c pytorch -c nvidia -c pytorch3d
conda activate shape_align
pip install pykeops biotite open3d plyfile ProDy pykeops rdkit==2022.9.5 tqdm==4.49.0 unidip pytorch-lightning
pip install git+https://github.com/hesther/espsim.git
  ```

## 2. download the needed prior models from [here](https://storage.googleapis.com/vantai-public-archive/shapelinker) and [here](https://github.com/MolecularAI/ReinventCommunity/blob/master/notebooks/models/linkinvent.prior)


## 3. direct sample

ShapeLinker already provides some trained RL agents. We can directly sample the molecules from them to save time. We provide the input json files in `jsons.zip`. Remember to change the path of model and output file in the json file. Use the code like this in the command:

- ```
python -u Reinvent/input.py sampling_config.json
  ```

## 4. train RL agent

The RL agents of other targets are not provided, so we need to train it. The corresponding json files are also provided in `jsons.zip`. Use the code like this in the command:

- ```
python Reinvent/input.py RL_Configuration.json
  ```

After training, return to step 3 to sample the molecules from trained agents. 