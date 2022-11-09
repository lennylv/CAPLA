# CAPLA

#####                      — improved prediction of protein-ligand binding affinity by a deep learning approach based on a cross-attention mechanism.

<div style ="text-align:justify">Accurate and rapid prediction of protein-ligand affinity is a great challenge currently encountered in drug discovery. Recent advances have manifested a promising alternative in applying deep learning-based computational approaches for accurately quantifying protein-ligand affinity. The structure complementarity between protein-binding pockets and ligands determines the binding strength between a protein and a ligand, but most of existing deep learning approaches usually extracted the features of pockets and ligands by two detached modules. In this work, a new deep learning approach based on the cross-attention mechanism named CAPLA was developed for improved prediction of protein-ligand binding affinity based on sequence-level information of both protein and ligand alone. Specifically, CAPLA employs the cross-attention mechanism to crossly attend protein-binding pocket and ligand features, and further employs the dilated convolution to capture multiscale long-range contextual features. We evaluated the performance of our proposed CAPLA on multitudinous benchmarking experiments on protein-ligand binding affinity prediction, demonstrating the superior performance of CAPLA over state-of-the-art baseline approaches. Moreover, we provided the interpretability for CAPLA to uncover critical functional residues that contribute most to the protein-ligand binding affinity through the analysis of the attention scores generated by the cross-attention mechanism. Consequently, these results indicated that CAPLA is an effective approach for protein-ligand affinity prediction and may contribute to useful guidance for further drug development.</div>

##### This source code was tested on the basic environment with `conda==4.8.2` and `cuda==11.3`

## Environment Reproduce

- In order to get CAPLA, you need to clone this repo:

  ```
  git clone git@github.com:lennylv/CAPLA.git
  cd CAPLA
  ```

- Unzip the "SourceCode.zip", "envs.zip" files into the current directory, and create environment using files provided in `./envs` directory

  ```
  unzip SourceCode.zip
  unzip envs.zip
  cd envs
  conda env create -f capla_conda.yaml
  pip install -r capla_pip.txt
  ```

- Install the apex in the environment (the package is provided in ./envs/apex)

  ```
  cd apex
  python setup.py install
  ```

## Run & Test

- Train your own model

  ```
  cd SourceCode/CAPLA/src
  python main.py
  ```

- Show the result in paper &  Test your own dataset

  ```
  cd SourceCode/CAPLA/src
  python test.py testset (e.g., Test2016_290, Test2016_262)
  ```



#### contact

Zhi Jin : 20214227052@stu.suda.edu.cn 

Tingfang Wu: tfwu@suda.edu.cn
