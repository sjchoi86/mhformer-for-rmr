# MHFormer for Robust Motion Retargeting
This repo contains a Python script for Human pose estimation with MHFormer for Robust Robot Motion Retargeting. Note that most of the Python scripts are forked from the [official MHFormer repo](https://github.com/Vegetebird/MHFormer) and modified slightly to be compatible with MAC and Ubuntu (i.e., mps and cuda). 

### Installation
- Create a conda environment: ```conda create -n mhformer python=3.9```
- Install PyTorch 1.13.1 and Torchvision 0.8.2 following the [official instructions](https://pytorch.org/)
- ```pip3 install -r requirements.txt```

### Download pretrained MHFormer model
The pretrained model can be found in [here](https://drive.google.com/drive/folders/1UWuaJ_nE19x2aM-Th221UpdhRPSCFwZa?usp=sharing), please download it and put it in the './checkpoint/pretrained' directory. 

### Download pretrained YOLOv3 and HRNet
The pretrained YOLOv3 and HRNet models can be found in [here](https://drive.google.com/drive/folders/1_ENAMOsPM7FXmdYRbkwbFHgzQq_B_NQA?usp=sharing), please download it and put it in the './demo/lib/checkpoint' directory. 

### Demo
Then, you need to put your in-the-wild videos in the './demo/video' directory. 

Run the command below:
```bash
python3 demo/run_mhformer.py --video sample_video.mp4 --devce mps
```

The pose estimation results will be saved into `demo/result/`.


