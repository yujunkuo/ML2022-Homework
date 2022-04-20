# HW6

## 執行方式

1. WGAN & WGAN-GP: Run with Jupyter Notebook

2. StyleGAN: 
    - Optional (For Multiple GPUs):
        - $ export CUDA_VISIBLE_DEVICES=1
    - Install:
        - $ pip install stylegan2_pytorch
    - Train:
        - $ stylegan2_pytorch --data ../faces --multi-gpus --image-size 64 --batch-size 1 --num-train-steps 40000 --gradient-accumulate-every 8
    - Generate:
        - $ for run in {1..1000}; do stylegan2_pytorch  --generate --num_image_tiles 1; done
    - Modify File Name
        - Run styleGAN.ipynb to modify file name


## 結果紀錄

- styleGAN Regular: 0.575 8567.92
- *(Best) styleGAN MR: 0.749 8422.84
- styleGAN EMA: 0.735 8465.07

## 參考資料

- WGAN: [WGAN-Link](https://github.com/eriklindernoren/PyTorch-GAN/blob/master/implementations/wgan/wgan.py)
- WGAN-GP: [WGAN-GP-Link](https://github.com/eriklindernoren/PyTorch-GAN/blob/master/implementations/wgan_gp/wgan_gp.py)
- StyleGAN: [StyleGAN-Link](https://github.com/lucidrains/stylegan2-pytorch)