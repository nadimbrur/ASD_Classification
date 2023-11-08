 Autism Spectrum Disorder Detection using Facial Images and Deep Learning
========
 

 

This repository contains implementation for Sequencer.

## Abstract
 Utilize CNN and LSTM features of facial images to diagnose ASD which is more robust than single model features.

## Schematic diagrams

The total block is:
![Modell](https://github.com/nadimbrur/ASD_Classification/assets/88606925/487bd884-ad49-40b7-bbe3-2f69dcb56f07)

The overall architecture of Sequencer2D is similar to the typical hierarchical ViT and Visual MLP. It uses Sequencer2D blocks instead of Transformer blocks:
 
![Sequencer]

Sequencer2D block replaces the Transformer's self-attention layer with an LSTM-based layer like BiLSTM2D layer:

![Sequencer2D]

BiLSTM2D includes a vertical LSTM and a horizontal LSTM:

![BiLSTM2D]

[Sequencer]: img/Sequencer.jpg
[Sequencer2D]: img/Sequencer2D.jpg
[BiLSTM2D]: img/BiLSTM2D.jpg

 

### Requirements
- torch>=1.10.0
- torchvision
- timm==0.5.4
- Pillow
- matplotlib
- scipy
- etc., see [requirements.txt](requirements.txt)

### Data preparation
Download and extract Kaggle :https://www.kaggle.com/datasets/imrankhan77/autistic-children-facial-data-set. The directory structure should be as follows.

```
│dataset/
├──Autistic/
│     ├── 6.JPEG
│     ├── 7.JPEG
│     ├── ...... 
├──Non-autisce/
│     ├── 8.JPEG
│     ├── 9.JPEG
│     ├── ......
```

 
 
 
