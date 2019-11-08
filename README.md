# Learning with Long-term Remembering: Following the Lead of Mixed Stochastic Gradient 
### https://arxiv.org/abs/1909.11763
Authors: Yunhui Guo*, Mingrui Liu*, Tianbao Yang, Tajana Rosing      
*Equal contribution

## Abstract
Current deep neural networks  can achieve remarkable performance on a single task. However, when the deep neural network is continually trained on a sequence of tasks, it seems to gradually forget the previous learned knowledge. This phenomenon is referred to as catastrophic forgetting and motivates the field called lifelong learning. The central question in lifelong learning is how to enable deep neural networks to maintain performance on old tasks while learning a new task. In this paper, we introduce a novel and effective lifelong learning algorithm, called MixEd stochastic GrAdient (MEGA), which allows deep neural networks to acquire the ability of retaining performance on old tasks while learning new tasks. MEGA modulates the balance between old tasks and the new task by integrating the current gradient with the gradient computed on a small reference episodic memory. Extensive experimental results show that the proposed MEGA algorithm significantly advances the state-of-the-art on all four commonly used lifelong learning benchmarks, reducing the error by up to 18%. 

## Requirements

TensorFlow >= v1.9.0.
The code is based on https://github.com/facebookresearch/agem.

## Training

To replicate the results of the paper on a particular dataset, execute (see the Note below for downloading the CUB and AWA datasets):
```bash
$ ./replicate_results.sh <DATASET> <THREAD-ID> 
```

Example runs are:
```bash
$ ./replicate_results.sh MNIST 4     /* Train MEGA on MNIST */

$ ./replicate_results.sh CIFAR 3     /* Train MEGA on CIFAR */

$ ./replicate_results.sh CUB 3 0   /* Train MEGA on CUB */

$ ./replicate_results.sh AWA 7 0    /* Train MEGA on AWA */
```

### Note
For CUB and AWA experiments, download the dataset prior to running the above script. Run following for downloading the datasets:

```bash
$ ./download_cub_awa.sh
```
The plotting code is provided under the folder `plotting_code/`. Update the paths in the plotting code accordingly.

### Results on MNIST
<p align="center">
<img src="https://github.com/yunhuiguo/MEGA/blob/master/figs/mnist_average_accuracy.png"  width="400" height="200">
  
### Results on CIFAR
<p align="center">
<img  src="https://github.com/yunhuiguo/MEGA/blob/master/figs/cifar_average_accuracy.png"  width="400" height="200">
  
### Results on CUB
<p align="center">
<img src="https://github.com/yunhuiguo/MEGA/blob/master/figs/cub_average_accuracy.png"  width="400" height="200">

  
### Results on AWA
<p align="center">
<img src="https://github.com/yunhuiguo/MEGA/blob/master/figs/awa_average_accuracy.png"  width="400" height="200">

### Legend
<p align="center">
<img src="https://github.com/yunhuiguo/MEGA/blob/master/figs/aa_legend.png">



If you find this repository useful in your own research, please consider citing:
```
@article{guo2019learning,
  title={Learning with Long-term Remembering: Following the Lead of Mixed Stochastic Gradient},  
  author={Guo, Yunhui and Liu, Mingrui and Yang, Tianbao and Rosing, Tajana},
  journal={arXiv preprint arXiv:1909.11763},
  year={2019}
}
```
