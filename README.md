# Accelerating convolutional neural network on GPUs

This is the source code of Accelerating convolutional neural network on GPUs. 

## Experiment environment

```
OS: Ubuntu 18.04
GPU: GTX 1080Ti
CUDA: 10.1, V10.1.243
CuDNN: 7.6
```
If you want to reproduct our experiment, please use same environment. We also the GTX 2080 to finishned our experiment. 

## Usage

```
$ git clone https://github.com/Darcy-Chen/Accelerating.git
$ cd Accelerating
$ wget https://www.dropbox.com/s/5yeny1wv0ayn481/dataset.zip?dl=0
$ mv 'dataset.zip?dl=0' dataset.zip
$ unzip dataset.zip
```

When running on Jetson using Docker Container, run this before installing:
```
apt-get update
apt-get install -y sudo
sudo apt-get install unzip
```

If you want to only using the code of convolution:

```
$ cd ECR
$ bash run_ecr_comparation.sh
```
Therefore, we can run the convolution and max pooling by the fellow steps:
```
$ cd PECR
$ bash run_pecr_comparation.sh
```

## Notes

- Change Makefile from /ECR/cudnn and /PECR/cudnn line 37, 245, 246 to match your local cudnn path, line 251 to match the architecture of the device

## License

MIT © Richard McRichface

