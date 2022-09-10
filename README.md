[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/proxzima/skin-cancer-mnist-resnet50-iv3-vgg16-19-googlenet)

<div align="center">

# Skin Cancer MNIST HAM10000

**Residual learning: a building block.**
</div>

<img align="left" src="https://raw.githubusercontent.com/kabartay/kaggle-siim-isic-melanoma-classification/master/materials/A-cell-from-the-Residual-Network-architecture-The-identity-connection-helps-to-reduce.png" width="350" style='margin-right:10px'/>
The degradation (of training accuracy) indicates that not all systems are similarly easy to optimize. In [Kaiming He et all. 2015] the degradation problem is adressed by introducing a deep residual learning framework. Instead of hoping each few stacked layers directly fit a desired underlying mapping, we explicitly let these layers fit a residual mapping. Formally, denoting the desired underlying mapping as H(x), we let the stacked nonlinear layers fit another mapping of F(x) := H(x)−x. The original mapping is recast into F(x)+x. We hypothesize that it is easier to optimize the residual mapping than to optimize the original, unreferenced mapping. To the extreme, if an identity mapping were optimal, it would be easier to push the residual to zero than to fit an identity mapping by a stack of nonlinear layers.

The formulation of F(x)+x can be realized by feedforward neural networks with ''shortcut connections'' (see scheme). Shortcut connections are those skipping one or
more layers. In our case, the shortcut connections simply perform identity mapping, and their outputs are added to the outputs of the stacked layers (see scheme). Identity shortcut connections add neither extra parameter nor computational complexity. The entire network can still be trained end-to-end by SGD with backpropagation, and can be easily implemented using common libraries

<br>
<br>

<div align="center">

**Example of ResNet50 vs Xception vs Inception-V3 vs VGG-19 vs VGG-16 as reference model.**
<img align="center" src="https://github.com/PROxZIMA/Skin-Cancer-MNIST-HAM10000/raw/master/assets/ResNet50%20vs%20Xception%20vs%20Inception-V3%20vs%20VGG-19%20vs%20VGG-16.png" width="870" />
</div>

<br>
<br>

<div align="center">

**Detailed example of GoogLeNet a.k.a. Inception-V1 (Szegedy, 2015) as reference model.**
<img align="center" src="https://github.com/PROxZIMA/Skin-Cancer-MNIST-HAM10000/raw/master/assets/GoogLeNet%20(Inception-V1).png" />
</div>


# References
- [Article] [Kaiming He et al Deep Residual Learning for Image Recognition. (CVPR 2015)](https://arxiv.org/abs/1512.03385)
- [Image] [A Basic Residual Block](https://medium.datadriveninvestor.com/developing-with-keras-functional-api-6017828408cd)
- [Image] [Deep Feature-Based Classifiers for Fruit Fly Identification (Diptera: Tephritidae)](https://www.researchgate.net/figure/VGG16-VGG19-Inception-V3-Xception-and-ResNet-50-architectures_fig1_330478807)
- [Image] [Googlenet/InceptionV1 architecture](https://developer.ridgerun.com/wiki/index.php?title=GstInference/Supported_architectures/InceptionV2)
- [Notebook] [skin cancer resnet50](https://www.kaggle.com/code/zhyaqi/skin-cancer-resnet50)
- [Notebook] [MinorProject_skinLesions](https://www.kaggle.com/code/nancybhargava/minorproject-skinlesions)
