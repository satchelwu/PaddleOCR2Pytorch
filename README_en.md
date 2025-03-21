# [PaddleOCR2Pytorch](https://github.com/frotms/PaddleOCR2Pytorch)

English | [简体中文](README.md)

## Introduction
Converting PaddleOCR to PyTorch.

This repository aims to 

- learn PaddleOCR
- use models in PyTorch which are trained in Paddle
- give a guideline for Paddle2PyTorch

## TODO

- [ ] AAAI 2021 end-to-end algorithm PGNet
- [ ] other text recognition models: RARE, SRN

## Notice

`PytorchOCR` models are converted from `PaddleOCRv2.0`.

**Recent updates**
- 2021.4.12 update STARNET
- 2021.4.8 update DB, SAST, EAST, ROSETTA, CRNN
- 2021.4.3 update more than 25+ multilingual recognition models [models list](./doc/doc_en/models_list_en.md), including：English, Chinese, German, French, Japanese，Spanish，Portuguese Russia Arabic and so on.  Models for more languages will continue to be updated [Develop Plan](https://github.com/PaddlePaddle/PaddleOCR/issues/1048).
- 2021.1.10 upload Chinese and English general OCR models.

## Features
- PTOCR series of high-quality pre-trained models, comparable to commercial effects
    - Ultra lightweight ptocr_mobile series models
    - General ptocr_server series models
    - Support Chinese, English, and digit recognition, vertical text recognition, and long text recognition
    - Support multi-language recognition: Korean, Japanese, German, French, etc.

## [Model List](./doc/doc_en/models_list_en.md) (updating)

PyTorch models in BaiduPan：https://pan.baidu.com/s/1r1DELT8BlgxeOP2RqREJEg code：6clx

PaddleOCR models in BaiduPan：https://pan.baidu.com/s/1getAprT2l_JqwhjwML0g9g code：lmv7 

If you want to get more models including multilingual models，please refer to [PTOCR  series](./doc/doc_en/models_list_en.md).

## Tutorials
- [Installation](./doc/doc_en/installation_en.md)
- [Inferences](./doc/doc_en/inference_en.md)
- [PP-OCR Pipeline](#PP-OCR-Pipeline)
- [Visualization](#Visualization)
- [Reference documents](./doc/doc_en/reference_en.md)
- [FAQ](https://github.com/PaddlePaddle/PaddleOCR/blob/release/2.0/doc/doc_en/FAQ_en.md)
- [References](#References)



<a name="PP-OCR-Pipeline"></a>

## PP-OCR Pipeline

<div align="center">
    <img src="./doc/framework.png" width="800">
</div>


PP-OCR is a practical ultra-lightweight OCR system. It is mainly composed of three parts: DB text detection[2], detection frame correction and CRNN text recognition[7]. The system adopts 19 effective strategies from 8 aspects including backbone network selection and adjustment, prediction head design, data augmentation, learning rate transformation strategy, regularization parameter selection, pre-training model use, and automatic model tailoring and quantization to optimize and slim down the models of each module. The final results are an ultra-lightweight Chinese and English OCR model with an overall size of 3.5M and a 2.8M English digital OCR model. For more details, please refer to the PP-OCR technical article (https://arxiv.org/abs/2009.09941). Besides, The implementation of the FPGM Pruner [8] and PACT quantization [9] is based on [PaddleSlim](https://github.com/PaddlePaddle/PaddleSlim).


## Visualization
- Chinese OCR model
<div align="center">
    <img src="./doc/imgs_results/ch_ptocr_mobile_v2.0/11.jpg" width="800">
    <img src="./doc/imgs_results/ch_ptocr_mobile_v2.0/00015504.jpg" width="800">
    <img src="./doc/imgs_results/ch_ptocr_mobile_v2.0/00056221.jpg" width="800">
    <img src="./doc/imgs_results/ch_ptocr_mobile_v2.0/1.jpg" width="800">
</div>


- English OCR model
<div align="center">
    <img src="./doc/imgs_results/ch_ptocr_mobile_v2.0/img_12.jpg" width="800">
</div>


- Multilingual OCR model
<div align="center">
    <img src="./doc/imgs_results/french_0.jpg" width="800">
    <img src="./doc/imgs_results/korean.jpg" width="800">
</div>


<a name="Reference"></a>

## References

- [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)
- [PytorchOCR](https://github.com/WenmuZhou/PytorchOCR)
- [Paddle](https://github.com/PaddlePaddle)
- [Pytorch](https://pytorch.org/)
- [https://github.com/frotms/image_classification_pytorch](https://github.com/frotms/image_classification_pytorch)
- [https://github.com/PaddlePaddle/PaddleOCR/blob/release/2.0/doc/doc_ch/models_list.md](https://github.com/PaddlePaddle/PaddleOCR/blob/release/2.0/doc/doc_ch/models_list.md)