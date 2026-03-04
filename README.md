The code provided here is for the  **Comprehensive assessment and benchmark of deep generative models for proteolysis targeting Chimera (PROTAC) design** paper and serves as an illustrative example of the metric calculations described in the manuscript.  



## 1. Data Preparation

* Prepare the generated molecule files in `.smi` format (here, `example1.smi` is used as an example). 
  



## 2. QED, SA score, SlogP, Number of stereo centers, and Tanimoto similarity ECF6

* REINVENT4 can conveniently calculate a wide range of basic physicochemical properties (alternatively, these properties can also be computed using RDKit). By following the [provided instructions](https://github.com/MolecularAI/REINVENT4/blob/main/configs/scoring.toml), the calculated metrics can be obtained. Here, `example2_reinvent.csv` is presented as an example output file. QED, SA score, SlogP, Number of stereo centers, and Tanimoto similarity ECF6 are averaged and used in the manuscript. 


* We provide all generated molecules (as well as the metrics calculated by REINVENT4) used in the manuscript as `data.zip`. If the model generates more than 250 molecules, only the first 250 are retained for metric calculation.
  



## 3. Retro*

* Retro* is used for predicting molecular retrosynthetic routes, and the calculations can be performed according to the code provided in [its repository](https://github.com/binghong-ml/retro_star). Using `example2_reinvent.csv` as an input file, the output file would be `example3_retro.csv`. The total Retro* score is the proportion of molecules for which a valid retrosynthetic route is successfully predicted.

 

## 4. Glide dock, Pharm Num and Pharm Value

* Use Schrödinger Maestro to dock the generated molecules and perform the pharmacophore screening. More details can be found in 'Molecular docking and pharmacophore screening' section of the manuscript. Save the Glide docking scores in `example4_glide.csv` and the pharmacophore screening scores in `example5_pharm.sdf` .



## 5. Autodock Vina

* The Vina score can be calculated following [its repository (version 1.2.7)](https://github.com/ccsb-scripps/AutoDock-Vina/releases). Calculate and save the vina scores in `example6_vina.csv` . 



## 6. Total score

* All needed files are done! If you want to calculate a total score as shown in the manuscript, you can refer to `score.ipynb`	 . 









