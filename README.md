# LVIS-INSTRUCT4V

## Introduction

We introduce a fine-grained visual instruction dataset, LVIS-INSTRUCT4V, which contains *220K* visually aligned and context-aware instructions produced by prompting the powerful GPT-4V with images from LVIS. Please refer to the [arxiv paper](https://arxiv.org/abs/2311.07574) for more details.

## Usage

Please follow [LLaVA](https://github.com/haotian-liu/LLaVA) to set up the code. 

LVIS-INSTRUCT4V is available at [LVIS-INSTRUCT4V](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V). To achieve better results on the QA benchmarks, we follow LLaVA 1.5 to mix LVIS-INSTRUCT4V with academic task related data (see the Table 1 & 7 in [LLaVA 1.5](https://arxiv.org/pdf/2310.03744.pdf) paper), which can be found at [LVIS-INSTRUCT4V-Nodetail-mix619k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-Nodetail-mix619k), [LVIS-INSTRUCT4V-mix730k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-mix730k), and [LVIS-Instruct4V-LLaVA-Instruct-mix880k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-LLaVA-Instruct-mix880k).


## Model Zoo
 |  Version | Data  | Size | Schedule | Checkpoint | VQAv2 | GQA | VizWiz | SQA | T-VQA | POPE | MME | MM-Bench | MM-Bench-CN | SEED | LLaVA-Bench-Wild | MM-Vet  | 
 | ---------- | ---------- | ---------- | ----------- | ----------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 
 |  LLaVA-1.5 | [LVIS-Instruct4V-Nodetail-mix619k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-Nodetail-mix619k) | 7B | full_ft-1e | [LVIS-Instruct4V-Nodetail-mix619k-7b](https://huggingface.co/X2FD/LVIS-Instruct4v-7b) | 79.2 | 62.6 | 52.5 | 68.4 | 57.6  | 84.0 | 1472.9 | 67.1 | 60.0 | 60.8 | 70.4 | 34.6 | 
 |  LLaVA-1.5 | [LVIS-Instruct4V-mix730k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-mix730k) | 7B | full_ft-1e | [LVIS-Instruct4V-mix730k-7b](https://huggingface.co/X2FD/LVIS-Instruct4V-mix730k-7b/tree/main)  | 79.4 |  62.6 | 52.6 | 68.9 | 58.4 | 85.1 | 1495.3 | 66.6 | 59.6 | 60.5 | 67.1 | 33.3  | 
 |  LLaVA-1.5 | [LVIS-Instruct4V-LLaVA-Instruct-mix880k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-LLaVA-Instruct-mix880k) | 7B | full_ft-1e | [LVIS-Instruct4V-LLaVA-Instruct-mix880k-7b](https://huggingface.co/X2FD/LVIS-Instruct4v-LLaVA-7b)  | 79.6 |  62.6 | 51.8 | 68.3 | 58.7 | 86.0 | 1528.2 | 66.2 | 60.4 | 60.6 | 67.0 | 31.5  | 
 |  LLaVA-1.5[^1] | [LVIS-Instruct4V-Nodetail-mix619k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-Nodetail-mix619k) | 13B | full_ft-1e | [LVIS-Instruct4V-Nodetail-mix619k-13b](https://huggingface.co/X2FD/LVIS-Instruct4v-13b) | 80.1 | 63.8 | 51.4 | 69.0 | 62.1 |  85.3 | 1572.0 | 67.8 | 61.0 | 62.5 | 76.7 | 40.2 |
 |  LLaVA-1.5 | [LVIS-Instruct4V-LLaVA-Instruct-mix880k](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V-LLaVA-Instruct-mix880k) | 13B | full_ft-1e | [LVIS-Instruct4V-LLaVA-Instruct-mix880k-13b](https://huggingface.co/X2FD/LVIS-Instruct4v-LLaVA-13b) | 80.7 | 63.6 |57.2 | 70.6 | 62.5 | 86.0 | 1574.9 | 68.0 | 61.1 | 61.6 | 71.3 | 37.4

[^1]: We find TextQA is sensitive to the beam number, and for 13B models, we use beam = 3 on TextQA.

## Reference

If you find our work useful for your research or applications, please cite using this BibTeX:

```
@article{wang2023instruct4v,
  title={To See is to Believe: Prompting GPT-4V for Better Visual Instruction Tuning},
  author={Wang, Junke and Meng, Lingchen and Weng, Zejia and He, Bo and Wu, Zuxuan and Jiang, Yu-Gang},
  journal={arXiv preprint arXiv:2311.07574},
  year={2023}
}
```


## Acknowledgement

We thank the authors of [LLaVA](https://github.com/haotian-liu/LLaVA) for their contribution to the open-source community.
