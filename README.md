# How to run this
- install Anaconda
  - (https://www.anaconda.com/docs/getting-started/anaconda/install)
- create conda environment with python 3.9
  - run `conda create --name fcgformer python=3.9` in the terminal
- activate the environment
  - `conda activate fcgformer`
- install required libraries
  - for everything except pytorch, run `pip install -r requirements.txt`
  - install pytorch
    - easiest: `pip install torch torchvision torchaudio` (this will run the model on the CPU)
    - (optionally) if you have an nvidia GPU, you can look online how to install the correct version for your gpu and operating system
      - this will make the model training much faster, but is not required if you just want to use the already trained model, which by default is downloaded from the internet
  - sign up to https://huggingface.co/
  - create a huggingface access token so that you can authorize your installation to download the dataset / trained model from huggingface
    - https://huggingface.co/settings/tokens/new?tokenType=read
  - run `huggingface-cli login` and enter the access token you created
  - open and try running the jupyter notebook `notebook.ipynb`
    - if you're using vscode, this can be opened and run via vscode
    - if not, run `jupyter lab` and it should open a programming environment in your browser where you can run the notebook.



# Below is the original documentation:

### :star: This is the official repo for our paper **Fcg-Former: Identification of Functional Groups in FTIR Spectra Using Enhanced Transformer-Based Model** published in Analytical Chemistry 2024 :star:

<p align="center">
      <a href="https://pubs.acs.org/doi/10.1021/acs.analchem.4c01622"><img alt="Google Scholar" src="https://img.shields.io/badge/DOI-10.1021/acs.analchem.4c01622-green?color=FF8000&logoColor=white"></a>
      <img alt="Python" src="https://img.shields.io/badge/Python%20-%2314354C.svg?style=flat-square&logo=python&logoColor=white" />
      <img alt="Pytorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white" />
      <img alt="Hugging Face" src="https://img.shields.io/badge/🤗_Hugging_Face-_oItsMineZ&logoColor=white" />
      <a href="https://github.com/lycaoduong/FcgFormer/stargazers"><img alt="Stargazers" src="https://img.shields.io/github/stars/lycaoduong/FcgFormer?style=for-the-badge&logo=github&color=f4dbd6&logoColor=D9E0EE&labelColor=302D41"></a>

</p>

# FcgFormer
- Author: lycaoduong
- Email: lycaoduong@gmail.com

## Dataset Download
Contact: lycaoduong@gmail.com

## For training
Run python script train.py with variable parser arguments:
```
--python train.py
```

## From Authors
- [x] Training code
    - [x] Release HuggingFace model
    - [x] Release training source code
- [x] Training environment
    - [x] Release Conda + Pip requirements.txt
    - [ ] Release Dockerfile
- [x] FTIRDataset
  - [x] Release HFSpace: https://huggingface.co/spaces/lycaoduong/FcgFormerApp 
  - [x] Release Dataset: https://huggingface.co/datasets/lycaoduong/FTIR
  - [x] Release Model Card: https://huggingface.co/lycaoduong/FcgFormer

# **Citation**
```@article{doan2024fcg,
  title={Fcg-Former: Identification of Functional Groups in FTIR Spectra Using Enhanced Transformer-Based Model},
  author={Doan, Vu Hoang Minh and Ly, Cao Duong and Mondal, Sudip and Truong, Thi Thuy and Nguyen, Tan Dung and Choi, Jaeyeop and Lee, Byeongil and Oh, Junghwan},
  journal={Analytical Chemistry},
  year={2024},
  publisher={ACS Publications}
}
