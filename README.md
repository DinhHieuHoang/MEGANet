# MEGANet: Multi-Scale Edge-Guided Attention Network for Weak Boundary Polyp Segmentation
Authors: Nhat-Tan Bui, Dinh-Hieu Hoang, Quang-Thuc Nguyen, Minh-Triet Tran, Ngan Le

## Introduction
<image src="Images/architecture.png">
  
Efficient polyp segmentation in healthcare plays a critical role in enabling early diagnosis of colorectal cancer. However, the segmentation of polyps presents numerous challenges, 
including the intricate distribution of backgrounds, variations in polyp sizes and shapes, and indistinct boundaries. Defining the boundary between the foreground (i.e. polyp itself) and the background (surrounding tissue) is difficult. To mitigate these challenges, we propose **M**ulti-Scale **E**dge-**G**uided **A**ttention Network (MEGANet) tailored specifically for polyp segmentation within colonoscopy images. This network draws inspiration from the fusion of a classical edge detection technique with an attention mechanism. 
By combining these techniques, MEGANet effectively preserves high-frequency information, notably edges and boundaries, which tend to erode as neural networks deepen. MEGANet is designed as an end-to-end framework, encompassing three key modules: an encoder, which is responsible for capturing and abstracting the features from the input image, a decoder, which focuses on salient features, and the Edge-Guided Attention module (EGA) that employs the Laplacian Operator to accentuate polyp boundaries. 
Extensive experiments, both qualitative and quantitative, on five benchmark datasets, demonstrate that our EGANet outperforms other existing SOTA methods under six evaluation metrics.

<image src="Images/EGA.png">

**Note that our model has been renamed. This means EGANet in the code file is now MEGANet in the paper.**

## Prerequisites
<ul>
  <li>Pytorch</li>
  <li>Torchvision</li>
  <li>Numpy</li>
  <li>Imageio</li>
  <li>SciPy</li>
  <li>Pillow</li>
</ul>

## Datasets and Trained Models
<ul>
</li>
  <li>Both <a href="https://drive.google.com/file/d/1YiGHLw4iTvKdvbT6MgwO9zcCv8zJ_Bnb/view">training</a> and <a href="https://drive.google.com/file/d/1Y2z7FD5p5y31vkZwQQomXFRB0HutHyao/view">testing</a> datasets are the same as 
  <a href="https://github.com/DengPingFan/PraNet">PraNet</a>. Downloading and moving it into the <code>data</code> folder.</li>
  <li>The MEGANet-ResNet version weights can be downloaded at <a href="https://drive.google.com/file/d/1qYL16oPEDvDl0s1lwSwdkMdThZnNBltW/view?usp=drive_link">Google Drive</a></li>
  <li>The MEGANet-Res2Net version weights can be downloaded at <a href="https://drive.google.com/file/d/12tPJwRpaBIGqbijMQIc5Y35uO0fX3J0d/view?usp=drive_link">Google Drive</a></li>
  <li>The Res2Net weights can be downloaded at <a href="https://drive.google.com/file/d/1Y_jNFU7uAcosb63o1fOt2IsLCh_KcfyG/view?usp=drive_link">Google Drive</a></li>
</ul>

## Usage

### Training

```python train.py --trainsize "training size" --train_path "path to train dataset" --train_save "path to save checkpoint"```

### Testing

```python test.py --testsize "testing size" --pth_path "path to checkpoint"```

### Evaluating

```python predict_score.py```

## Predictions

## Citation

## Acknowledgment
Par code is  these excellent works PraNet, EAGRNet and MSEG, which have provided the basis for our framework.
