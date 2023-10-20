## Generative Gradual Domain Adaptation with Optimal Transport (GOAT)

This is the official implementation for the algorithm **G**radual D**O**main **A**daptation with Optimal **T**ransport (GOAT) in the paper "Gradual Domain Adaptation: Theory and Algorithms."

# Install the repo
```
git clone https://github.com/yifei-he/GOAT.git
cd GOAT
pip install -r requirements.txt
```

# Prepare Data

The covertype dataset can be downloaded from: https://archive.ics.uci.edu/dataset/31/covertype. 

The portraits dataset can be downloaded from [here](https://www.dropbox.com/s/ubjjoo0b2wz4vgz/faces_aligned_small_mirrored_co_aligned_cropped_cleaned.tar.gz?dl=0). We follow the same data preprocessing procedure from https://github.com/p-lambda/gradual_domain_adaptation. Namely after downloading, extract the tar file, and copy the "M" and "F" folders inside a folder called dataset_32x32 inside the current folder. Then run "python create_dataset.py".

# Run Experiment
To run experiments, follow the following syntax.
```
python experiments.py --dataset color_mnist --gt-domains 1 --generated-domains 2
```
Here, `dataset` can be selected from `[mnist, portraits, covtype, color_mnist]`; `gt-domains` and `generated-domains` are the number of given ground-truth intermediate domains (only available for the two MNSIT datasets) and domains generated by GOAT respectively, both default to be 0.

# Citation
