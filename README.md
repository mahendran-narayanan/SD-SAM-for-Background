# Stable Diffusion, Segment Anything models for replacing background in generated images

Using Stable diffusion (SD) model and Segment Anything model from Meta (SAM) for removing the background and add newer background for the image. Created with a Multi model pipeline.

## Stable Diffusion model

Huggingface Link : [CompVis/stable-diffusion-v1-4](https://huggingface.co/CompVis/stable-diffusion-v1-4)

Model Link : [Model](https://huggingface.co/CompVis/stable-diffusion-v1-4/tree/main)

Stable Diffusion is the diffusion model which generates images based on the text input. Stable Diffusion model is created by the researcheres from CompVis, StabilityAI and LAION.

The model is trained on LAION-5b dataset which contains 5.85 billion CLIP-filtered image-text pairs. The model is used to generate the images and the background needed for the images. We use the Stable diffusion v1-4 checkpoint. This particular model is being created by finetuning on v1-2 checkpoint with 225k steps at a resolution of 512x512.

## Segment Anything (SAM)

Huggingface link: [facebook/sam-vit-base](https://huggingface.co/facebook/sam-vit-base)

Model Link : [Model](https://segment-anything.com/)

Segment Anything Model (SAM) is used to produce object masks for the input image. SAM model is created by researchers from Meta. This model is trained on 11 million images and 1.1 billion masks. The model type is SAM-ViT consists of ViT Encoder, Prompt Encoder, Mask Decoder and The Neck.

The model is used for extracting the object from the SD output.

## Steps
1. Generate image and background using SD
2. Extract the object
3. Merge the resultant with SD.

![SD-SAM-working](https://github.com/mahendran-narayanan/SD-SAM-for-Background/blob/main/Pictures/SD-SAM-working.jpg)

## References
1. Stable Diffusion model
```
@InProceedings{Rombach_2022_CVPR,
    author    = {Rombach, Robin and Blattmann, Andreas and Lorenz, Dominik and Esser, Patrick and Ommer, Bj\"orn},
    title     = {High-Resolution Image Synthesis With Latent Diffusion Models},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2022},
    pages     = {10684-10695}
}
```
2. Segment Anything by Meta
```
@article{kirillov2023segment,
  title={Segment anything},
  author={Kirillov, Alexander and Mintun, Eric and Ravi, Nikhila and Mao, Hanzi and Rolland, Chloe and Gustafson, Laura and Xiao, Tete and Whitehead, Spencer and Berg, Alexander C and Lo, Wan-Yen and others},
  journal={arXiv preprint arXiv:2304.02643},
  year={2023}
}
```