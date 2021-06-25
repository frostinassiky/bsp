# BSP


This repo will hold the codes of paper: "[Boundary-sensitive Pre-training for Temporal Localization in Videos](https://arxiv.org/abs/2011.10830)". 

**We will update this repo once we get the approval to release our code.**


## Update

6 May 2021: We sent our code for feature extraction of pre-trained models for approval.

## Overview
Many video analysis tasks require temporal localization
for the detection of content changes. However, most existing
models developed for these tasks are pre-trained on general
video action classification tasks. This is due to large scale
annotation of temporal boundaries in untrimmed videos being expensive. Therefore, no suitable datasets exist that enable pre-training in a manner sensitive to temporal boundaries. In this paper for the first time, we investigate
model pre-training for temporal localization by introducing
a novel boundary-sensitive pretext (BSP) task. Instead of relying on costly manual annotations of temporal boundaries,
we propose to synthesize temporal boundaries in existing
video action classification datasets. By defining different
ways of synthesizing boundaries, BSP can then be simply
conducted in a self-supervised manner via the classification
of the boundary types. This enables the learning of video
representations that are much more transferable to downstream temporal localization tasks. Extensive experiments
show that the proposed BSP is superior and complementary to the existing action classification-based pre-training
counterpart, and achieves new state-of-the-art performance
on several temporal localization tasks.


[Arxiv](https://arxiv.org/pdf/2011.10830.pdf).

## Installation

1. Create conda environment
    ```shell script
    conda env create -f env.yml
    source activate gtad
    ```

### Data setup

TBD

## Code Architecture

    bsp                         # this repo
    ├── arch                    # difference video backbone
    ├── localization            # link to localization repo, e.g. gtad 
    ├── ops                     # video model, dataset, etc
    ├── tools                   # pack/unpack datasets
    ├── ckpt                    # pretrained models
    └── ...

## feature extraction
After downloading the pre-trained model and setting up the environment, you can start from the following script.

```shell script
python3 scripts/feature_extraction/activitynet_extract_features.py \
    <partition (train/val/test)> \ 
    <path_to_activitynet> \
    <network_weights> \
    <features folder> \
    <OPT:arch>
```

For example, 
```shell script
python3 scripts/feature_extraction/activitynet_extract_features.py train 
    <path_to_activitynet> \
    ckpt/TSM_r18_k400_cls_baseline/ckpt.best.pth.tar \
    features/activitynet tsm
```

Then, you may want to test the feature via localization repo, e.g. gtad
```shell script
cd localization/gtad
bash gtad.sh
```


If everything goes well, you can get the following result:
```
TBD
```

## Bibtex
Arxiv Version.
```text
@misc{xu2021boundarysensitive,
      title={Boundary-sensitive Pre-training for Temporal Localization in Videos}, 
      author={Mengmeng Xu and Juan-Manuel Perez-Rua and Victor Escorcia and Brais Martinez and Xiatian Zhu and Li Zhang and Bernard Ghanem and Tao Xiang},
      year={2021},
      eprint={2011.10830},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

## Contact
mengmeng.xu[at]kaust.edu.sa
