# SD-SAM-for-Background

Using Stable diffusion (SD) model and Segment Anything model from Meta (SAM) for removing the background and add newer background for the image. Created with a Multi model pipeline.

## Stable Diffusion model

Hugging Face Link : [CompVis/stable-diffusion-v1-4](https://huggingface.co/CompVis/stable-diffusion-v1-4)

Model Link : [Model](https://huggingface.co/CompVis/stable-diffusion-v1-4/tree/main)

Stable Diffusion is the diffusion model which generates images based on the text input. Stable Diffusion model is created by the researcheres from CompVis, StabilityAI and LAION. The model is trained on LAION-5b dataset which contains 5.85 billion CLIP-filtered image-text pairs.

The model is used to generate the images and the background needed for the images. We use the Stable diffusion v1-4 checkpoint. This particular model is being created by finetuning on v1-2 checkpoint with 225k steps at a resolution of 512x512.

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