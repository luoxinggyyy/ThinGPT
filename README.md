# Intelligent identification method of rock thin section based on multi-modal large language model


## Project profile
The proposed project is based on the CLIP model and GPT2, drawing on the ideas of CLIPCAP and the network foundation framework, which aims to generate long text descriptions for rock flakes. It is worth noting that the results of the model generation are in both Chinese and English. Since the data set I used was in Chinese, the pre-trained model provided was also generated in Chinese. If you need to generate the English version directly, then the data set can be replaced in English.


## Usage method
### Quick Start
To install dependency packages:
```
pip install -r requirements.txt
```
Directly generated using pre-trained models
1.Put the ThinGPT pre-trained model into output/mlp_finetune/
（https://drive.google.com/file/d/16Y1cfCB8PKpifyqhmdtkko3a4kMHV6xO/view?usp=sharing）

2.Place the GPT2 pre-trained model (which contains three files) in a folder called pretrain_models/
（https://drive.google.com/drive/folders/1RpxWfBur_P6l8EFzPMMzYuPiL_BFpZ6b?usp=sharing）

3.Put the CLIP pre-training model into pretrain_models/
（https://drive.google.com/file/d/1ZHyLBYopyPMmxT_p-24rSZfFFVA1E1eG/view?usp=sharing）

4.The images of the rock slices tested were placed in dataset/test1/
We have provided test images.
5.Run the following code in the terminal debugger
```
bash scripts/predict_finetune_gpt2.sh
```
The generated results are saved in the ouput folder


If you want to start training again, follow these steps:
1. Data preprocessing (encode your rock flake data set to generate picture-text pairs to get train.pkl) :
```
python process_flickr.py
```

2. Training
```
bash scripts/train_finetune_gpt2.sh
```

## Acknowledgments
This project is inspired by the (https://github.com/yangjianxin1/ClipCap-Chinese.git), thanks to the contribution of this project.

## REFERENCE
- https://github.com/openai/CLIP
- https://github.com/Morizeyao/GPT2-Chinese.git
- https://github.com/rmokady/CLIP_prefix_caption

- Connection
- email: b22010034@s.upc.edu.cn









