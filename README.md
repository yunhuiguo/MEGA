## Requirements

TensorFlow >= v1.9.0.

## Training

To replicate the results of the paper on a particular dataset, execute (see the Note below for downloading the CUB and AWA datasets):
```bash
$ ./replicate_results_iclr20.sh <DATASET> <THREAD-ID> 
```

Example runs are:
```bash
$ ./replicate_results_iclr20.sh MNIST 4     /* Train MEGA on MNIST */

$ ./replicate_results_iclr20.sh CIFAR 3     /* Train MEGA on CIFAR */

$ ./replicate_results_iclr20.sh CUB 3    /* Train MEGA on CUB */

$ ./replicate_results_iclr20.sh AWA 7     /* Train MEGA on AWA */
```

### Note
For CUB and AWA experiments, download the dataset prior to running the above script. Run following for downloading the datasets:

```bash
$ ./download_cub_awa.sh
```
The plotting code is provided under the folder `plotting_code/`. Update the paths in the plotting code accordingly.
