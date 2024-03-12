---
author: bobo
pubDatetime: 2024-03-12
title: 文生图技术总结
postSlug: text-to-image--summary
featured: true
draft: false
tags:
  - 文生图

description: 文生图
---

# 文生图

## Stable Diffusion知识

快速了解Stable Diffusion：https://www.comflowy.com/zh-CN/basics/prompt

SD官方模型能力介绍：https://stability.ai/news

SD模型的论文:
Original SD paper -- [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
SDXL paper -- [SDXL: Improving Latent Diffusion Models for High-Resolution Image Synthesis](https://arxiv.org/abs/2307.01952)
ControlNet paper -- [Adding Conditional Control to Text-to-Image Diffusion Models](https://arxiv.org/abs/2302.05543)

文生图提示词：
提示词介绍: https://learnprompting.org/zh-Hans/docs/image_prompting/intro
prompt hero: https://prompthero.com/

SD在线试用网站:
[Playground AI](https://playgroundai.com/)
[Stable Diffusion v1.5 demo](https://huggingface.co/spaces/runwayml/stable-diffusion-v1-5)
[Mage Space](https://www.mage.space/)

开源文生图模型分享社区：https://civitai.com/
开源文生图模型: https://huggingface.co/models?pipeline_tag=text-to-image&sort=trending

# 有特点的模型

IP-Adapter：https://github.com/tencent-ailab/IP-Adapter
人物适配

InstantID: https://instantid.github.io
只需一张人脸照片 几秒钟就能生成不同风格的人物照片，与传统方法需要多张参考图像和复杂的微调过程不同，InstantID 只需一张图像，而且无需复杂的训练或微调过程。能够满足高保真度的个性化图像生成，无需复杂的训练或微调过程。兼容性强，面部保真度和文本编辑性高，应用场景多样化、实用性和效率高、支持多重参考以获得更多的信息和灵感，增强生成图像的丰富性和多样性。

PhotoMaker: https://huggingface.co/spaces/TencentARC/PhotoMaker
利用多张照片作为身份 ID，获取人物特征，然后创造出一个新的、个性化的人物图像。能根据描述生成符合描述的人物照片，也能把几个不同人的照片特征混合在一起，创造出一个全新的人物形象。还能改变照片人物的性别、年龄和生成多种风格的其他照片。快速逼真，效果自然。

ControlNet：https://github.com/lllyasviel/ControlNet
控制生成图像的结构、人物姿态pos、深度

Layer Diffsion: https://github.com/layerdiffusion/sd-forge-layerdiffuse
生成透明的png图，如花朵、花瓶等

# 相关产品

heygen: https://www.heygen.com/
制作数字人

DID: https://www.d-id.com/
产品效果: https://clips-api-results.d-id.com/welcome_video.mp4
制作数字分身

krea ai: https://www.krea.ai/home
实时生成图像

Runway Multi Motion Brush: https://academy.runwayml.com/
控制图片运动。产品效果: https://www.youtube.com/watch?v=zQ3fQt8swEI&t=105s

OOTDiffusion：https://huggingface.co/spaces/levihsu/OOTDiffusion
AI换装

Elevenlabs: https://elevenlabs.io/
声音生成、声音克隆
