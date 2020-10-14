# Improved Schemes for Episodic Memory-based Lifelong Learning

Authors: Yunhui Guo*, Mingrui Liu*, Tianbao Yang, Tajana Rosing      
*Equal contribution

### NeurIPS 2020 (Spotlight)

### https://arxiv.org/abs/1909.11763 

```
@article{guo2019learning,
  title={Learning with Long-term Remembering: Following the Lead of Mixed Stochastic Gradient},  
  author={Guo, Yunhui and Liu, Mingrui and Yang, Tianbao and Rosing, Tajana},
  journal={arXiv preprint arXiv:1909.11763},
  year={2019}
}
```


## Abstract
Current deep neural networks can achieve remarkable performance on a singletask. However, when the deep neural network is continually trained on a sequenceof tasks, it seems to gradually forget the previous learned knowledge. This phe-nomenon is referred to ascatastrophic forgettingand motivates the field calledlifelong learning. Recently, episodic memory based approaches such as GEM [1]and A-GEM [2] have shown remarkable performance. In this paper, we providethe first unified view of episodic memory based approaches from an optimization’sperspective. This view leads to two improved schemes for episodic memory basedlifelong learning, called MEGA-I and MEGA-II. MEGA-I and MEGA-II modulatethe balance between old tasks and the new task by integrating the current gradientwith the gradient computed on the episodic memory. Notably, we show that GEMand A-GEM are degenerate cases of MEGA-I and MEGA-II which consistentlyput the same emphasis on the current task, regardless of how the loss changesover time. Our proposed schemes address this issue by using novel loss-balancingupdating rules, which drastically improve the performance over GEM and A-GEM.Extensive experimental results show that the proposed schemes significantly ad-vance the state-of-the-art on four commonly used lifelong learning benchmarks,reducing the error by up to 18%.

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
