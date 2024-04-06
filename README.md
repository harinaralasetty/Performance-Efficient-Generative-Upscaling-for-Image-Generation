# Performance Efficient Generative Upscaling for Image Generation
I've developed an optimized pipeline that leverages the power of diffusion models for initial image generation, followed by computationally efficient super-resolution upscaling using ESRGAN. This approach maintains photorealism and control over image details while successfully addressing high resolution requirements within resource constraints.
![image](https://github.com/harinaralasetty/Performance-Efficient-Generative-Upscaling-for-Image-Generation/blob/main/Performance%20Efficient%20Generative%20Upscaling.png)

# Abstract
This research explores the challenges and optimization strategies for generating high-resolution (2048 x 2048) photorealistic images depicting people and backgrounds from text descriptions. I focus on maximizing photorealism, steerability, and resource efficiency in the context of limited computational resources (Kaggle's P100 GPUs).  A combination of diffusion models specialized in photorealism and super-resolution techniques is employed to overcome resolution constraints.

# Introduction
Diffusion models, specifically Stable Diffusion and its variants, have revolutionized image synthesis. However, directly generating high-resolution images remains computationally intensive. This paper investigates a pipeline I developed that combines diffusion models for initial image generation and subsequent upscaling techniques to achieve the desired resolution while preserving photorealism and steerability.

# Methodology
## Model Selection
I explored the following models known for photorealism, with a particular emphasis on generating human figures:

stabilityai/stable-diffusion-xl-base-1.0 <br>
SG161222/Realistic_Vision_V6.0_B1_noVAE <br>
emilianJR/epiCRealism <br>
emilianJR/CyberRealistic_V3 <br>

Initial Generation: Experimentation focused on the models' ability to generate images based on text prompts while staying within the limitations of a P100 GPU.

## Upscaling
Due to resolution constraints, I adopted ESRGAN, a computationally efficient super-resolution technique, to upscale the generated images to 2048 x 2048.

## Evaluation
I evaluated the models and pipeline based on the following criteria:

Photorealism: Assessment of realistic lighting, textures, and the quality of human figures. <br>
Steerability: The ability to control and modify image details based on variations in the text prompt. <br>
Efficiency: Computation time and resource usage on the P100 GPU. <br>

# Result
My experimental pipeline demonstrated the following:

## Improved Resolution
The combination of diffusion models and ESRGAN successfully generated high-resolution images that met the requirements.

## Optimized Resource Usage
Upscaling smaller images allowed me to remain within computational limits while producing superior output compared to direct high-resolution generation attempts.

# Conclusion
This study highlights the potential of combining diffusion models with upscaling techniques for high-resolution image generation under computational constraints. It underscores the importance of model selection tailored to photorealism and efficient resource utilization strategies.

Kaggle notes: [Performance Efficient Image Generation | SD+ESRGAN](https://www.kaggle.com/code/hknaralasetty/performance-efficient-image-generation-sd-esrgan#Image-Generation)
