# Adaptive Segmentation Mask Attack

This repository contains the implementation of the _Adaptive Segmentation Mask Attack (ASMA)_, a targeted adversarial example generation method for deep learning segmentation models. This attack was proposed in the paper "_Impact of Adversarial Examples on Deep Learning Models for Biomedical Segmentation._" by _U. Ozbulak et al._ and published in the 22nd International Conference on Medical Image Computing and Computer Assisted Intervention, MICCAI-2019.

<br /> 
<img src="https://raw.githubusercontent.com/utkuozbulak/adaptive-segmentation-mask-attack/master/data/repository_examples/adversarial_optimization.gif">

## Citation
If you find the code in this repository relevant to your research, consider citing our paper. Also, feel free to use any visuals available here.

	@article{,
	  author = {},
	  title = {},
	  year = {},
	  publisher = {},
	  journal = {}
	}

## General Information
This repository is organized as follows:
* **Code** - *src/* folder contains necessary python files to perform the attack and calculate various stats (i.e., correctness and modification)

* **Data** - *data/* folder contains a couple of examples for testing purposes. The data we used in this study can be taken from [1].
  
* **Model** - Example model used in this repository can be downloaded from https://www.dropbox.com/s/6ziz7s070kkaexp/eye_pretrained_model.pt . _helper_functions.py_ contains a function to load this file and _main.py_ contains an exaple that uses this model.

## Frequently Asked Questions (FAQ)

* How can I run the demo? 

  **1-** Download the model from https://www.dropbox.com/s/6ziz7s070kkaexp/eye_pretrained_model.pt
  
  **2-** Create a folder called _model_ on the same level as _data_ and _src_, put the model under this (_model_) folder.
  
  **3-** Run _main.py_.

* Would this attack work in multi-class segmentation models?

  Yes, given that you provide a proper target mask.
  
* Does the code require modifications in order to make it work for multi-class segmentation models?

  No (probably, depending on your model/input).
  

## Requirements
```
python > 3.5
torch >= 0.4.0
torchvision >= 0.1.9
numpy >= 1.13.0
PIL >= 1.1.7
```

## References
[1]  Pena-Betancor C., Gonzalez-Hernandez M., Fumero-Batista F., Sigut J., Medina-Mesa E., Alayon S., Gonzalez M. _Estimation of the relative amount of hemoglobin in the cup and neuroretinal rim using stereoscopic color fundus images._

[2] Ronneberger, O., Fischer, P., Brox, T. _U-Net: Convolutional networks for biomedical image segmentation._
