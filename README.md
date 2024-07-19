# M3Net: Few-Shot Fine-Grained Action Recognition via Bidirectional Attention and Contrastive Meta-Learning

Official repository of ACM MM 2023 paper "_M3Net: Few-Shot Fine-Grained Action Recognition via Bidirectional Attention and Contrastive Meta-Learning_"

Due to the scarcity of manually annotated data required for fine-grained video understanding, few-shot fine-grained (FS-FG) action recognition has gained significant attention, with the aim of classifying novel fine-grained action categories with only a few labeled instances. Despite the progress made in FS coarse-grained action recognition, current approaches encounter two challenges when dealing with the fine-grained action categories: the inability to capture subtle action details and the insufficiency of learning from limited data that exhibit high intra-class variance and inter-class similarity. To address these limitations, we propose M3Net, a matching-based framework for FS-FG action recognition, which incorporates *multi-view encoding*, *multi-view matching*, and *multi-view fusion* to facilitate embedding encoding, similarity matching, and decision making across multiple viewpoints. *Multi-view encoding* captures rich contextual details from the intra-frame, intra-video, and intra-episode perspectives, generating customized higher-order embeddings for fine-grained data. *Multi-view matching* integrates various matching functions enabling flexible relation modeling within limited samples to handle multi-scale spatio-temporal variations by leveraging the instance-specific, category-specific, and task-specific perspectives. *Multi-view fusion* consists of matching-predictions fusion and matching-losses fusion over the above views, where the former promotes mutual complementarity and the latter enhances embedding generalizability by employing multi-task collaborative learning. Explainable visualizations and experimental results on three challenging benchmarks demonstrate the superiority of M3Net in capturing fine-grained action details and achieving state-of-the-art performance for FS-FG action recognition.


## Download Data

The evaluations are performed on two publicly released fine-grained action recognition datasets: _FineGym_ and _Diving48_.

### FineGym

Please visit the official site of [FineGym](https://sdolivia.github.io/FineGym/) to 
download data and extract frames for video clips with _Gym99_ and _Gym288_ annotations.

### Diving48

Please visit the official site of [Diving48](http://www.svcl.ucsd.edu/projects/resound/dataset.html/) and download the RGB file of the dataset. 

## Few-Shot Learning Protocols

You can find the split files of our few-shot fine-grained action recognition benchmarks [here](/benchmarks).
The specific training/test protocols of _Gym99_, _Gym288_ and _Diving48_ are introduced 
in Sec. 4.1 of our paper.

For each benchmark, "_trainlist.txt_" , "_vallist.txt_" and "_testlist.txt_" contain the labels 
of train/val/test categories. 

If you find this repository useful, please cite:

```
@inproceedings{tang2023m3net,
  title={M3net: multi-view encoding, matching, and fusion for few-shot fine-grained action recognition},
  author={Tang, Hao and Liu, Jun and Yan, Shuanglin and Yan, Rui and Li, Zechao and Tang, Jinhui},
  booktitle={Proceedings of the 31st ACM international conference on multimedia},
  pages={1719--1728},
  year={2023}
}
```