# indoor_outdoor_classification
Classify your pictures by classes indoor and outdoor with a CNN implemented with keras and tensorflow as backend!

## Predict your images:
```
python prediction.py --path path/to/your/image/directory
```
Running the evaluate script results in a .csv-file composed of two columns (filename, classlabel). The pretrained model is used for this step.

## Copy them into seperate directories:
```
python partition.py --path path/to/your/image/directory
```
Running the partition script results in two directiores in the results dir containing the final partition of the images.
  
## Train the model w/ your own day/night images:
Your train data has to be divided into two directories [../data/indoor, ../data/outdoor]
```
python train.py --path path/to/your/train/data
```
Running the train script results in weights.h5 file and overwrites the previous one. For transfer learning Inception-ResNet V2 model is used, with weights pre-trained on ImageNet.

## Authors
* Şiyar Yıkmış

## Acknowledgments

* CrowdHuman: A Benchmark for Detecting Human in a Crowd
* A. Pronobis, B. Caputo, P. Jensfelt, and H. I. Christensen. A discriminative approach to robust visual place recognition. In Proceedings of the IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS06), Beijing, China, October 2006.
