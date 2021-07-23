# Panoramic X-Ray Image Semantic Segmentation with TransUnet
The unofficial implementation of [TransUNet: Transformers Make Strong Encoders for Medical Image Segmentation](https://arxiv.org/abs/2102.04306) on Pytorch

![GZSL](./assets/outs.png "GZSL")
*Output of my implementation. (A) Original X-Ray Image; (B) Merged Image of the Predicted Segmentation Map and Original X-Ray; (C) Ground Truth; (D) Predicted Segmentation Map*

## TransUNet
- On various medical image segmentation tasks, the ushaped architecture, also known as U-Net, has become the de-facto standard and achieved tremendous success. However, due to the intrinsic
locality of convolution operations, U-Net generally demonstrates limitations in explicitly modeling long-range dependency. [1]
- TransUNet employs a hybrid CNN-Transformer architecture to leverage both detailed high-resolution spatial information from CNN features and the global context encoded by Transformers. [1]

## Model Architecture
![Model Architecture](./assets/arch.png "Model Architecure")
*TransUNet Architecture Figure from Official Paper*

## Dependencies
- Python 3.6+
- `pip install -r requirements.txt`

## Dataset
- UFBA_UESC_DENTAL_IMAGES[2] dataset was used for training.
- Dataset can be accessed by demand[3].

## Training
- Training process can be started with following command.
    - `python main.py --mode train --model_path ./path/to/model --train_path ./path/to/trainset --test_path ./path/to/testset `

## Inference
- After model is trained, inference can be run with following command.
    - `python main.py --mode inference --model_path ./path/to/model --image_path ./path/to/image
`

## References
- [1] [TransUNet: Transformers Make Strong Encoders for Medical Image Segmentation](https://arxiv.org/abs/2102.04306)
- [2] [Automatic segmenting teeth in X-ray images: Trends, a novel data set, benchmarking and future perspectives](https://www.sciencedirect.com/science/article/abs/pii/S0957417418302252)
- [3] [GitHub Repository of Dataset](https://github.com/IvisionLab/dental-image)