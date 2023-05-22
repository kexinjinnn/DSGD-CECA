# DSGD-CECA: Decentralized SGD with Communication-Optimal Exact Consensus Algorithm

This code repository is for the paper
**CDSGD-CECA: Decentralized SGD with Communication-Optimal Exact Consensus Algorithm** which will 
appear in ICML 2023. 

## Setup the environment

This code was trained and tested with

1. Python 3.7.5
2. PyTorch 1.4.0
3. Torchvision 0.5.0
4. tqdm 4.62.3
5. tensorboardX 2.4

Before running the deep learning code, please download and install BlueFog from https://github.com/Bluefog-Lib/bluefog. We highly recommend you install it via Docker, see the instructions in https://bluefog-lib.github.io/bluefog/docker.html. Pull the steady version gpu-0.3.0 in https://hub.docker.com/r/bluefoglib/bluefog/tags. 

## Train a model with DSGD-CECA

We recommend downloading all data before training and putting them in a local folder. The following code is to run MNIST experiment with 17 computing nodes using CECA-2P.

```bash
$ cd deep_learning/
$ bfrun -np 17 python mnist_main.py --dataset=mnist --lr=0.03 --epochs=20
```
## Test EquiTopo on synthetic data

We test the performances of EquiTopos using sythetic data to validate 
1) network-size-independent consensus rate (consensus.ipynb);
2) comparison with other commonly-used topologies in consensus rate (consensus.ipynb);
3) comparison with other commonly-used topologies in DSGD for strongly-convex problems (DSGD_convex.ipynb).

## EquiTopo comparison on MNIST and CIFAR-10

We test the performance of CECA-2P on MINIST and CIFAR-10.

### Performance on MNIST and CIFAR-10

| Method  | MNIST Acc. | CIFAR-10 Acc. |
|--------|------|------|
| CECA-2P | 98.34% | 92.07% |

## Citation

If you use this library or find the doumentation useful for your research, please consider citing:

Lisang Ding, Kexin Jin, Bicheng Ying, Kun Yuan, Wotao Yin,
**DSGD-CECA: Decentralized SGD with Communication-Optimal Exact Consensus Algorithm**.
ICML, 2023.

```txt
@inproceedings{Ding_2023_CECA,
    title = {DSGD-CECA: Decentralized SGD with Communication-Optimal Exact Consensus Algorithm},
    author = {Lisang Ding, Kexin Jin, Bicheng Ying, Kun Yuan, Wotao Yin},
    booktitle = {ICML},
    year = {2023}
}
```

