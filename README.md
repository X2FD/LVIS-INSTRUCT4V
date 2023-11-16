# LVIS-INSTRUCT4V

## Introduction

We introduce a fine-grained visual instruction dataset, LVIS-INSTRUCT4V, which contains *220K* visually aligned and context-aware instructions produced by prompting the powerful GPT-4V with images from LVIS. Please refer to the [arxiv paper](https://arxiv.org/abs/2311.07574) for more details.

## Usage

Please follow [LLaVA](https://github.com/haotian-liu/LLaVA) to set up the code. 

Our data is available at [LVIS-INSTRUCT4V](https://huggingface.co/datasets/X2FD/LVIS-Instruct4V)


## Model Zoo
 |  Version | Data  | Size | Schedule | Checkpoint | VQAv2 | GQA | VizWiz | SQA | T-VQA | POPE | MME | MM-Bench | MM-Bench-CN | SEED | LLaVA-Bench-Wild | MM-Vet  | 
 | ---------- | ---------- | ---------- | ----------- | ----------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 
 |  LLaVA-1.5 | LVIS-Instrcut4V | 7B | full_ft-1e | [LVIS-Instruct4v-7b](https://huggingface.co/X2FD/LVIS-Instruct4v-7b) | 79.2 | 62.6 | 52.5 | 70.3 | 57.6  | 84.0 | 1472.9 | 67.1 | 67.1 | 60.8 | 70.4 | 34.6 | 
 |  LLaVA-1.5 | LVIS-Instrcut4V + LLaVA-Instruct | 7B | full_ft-1e | [LVIS-Instruct4v-LLaVA-7b](https://huggingface.co/X2FD/LVIS-Instruct4v-LLaVA-7b)  | 79.6 |  62.6 | 51.8 | 70.1 | 58.7 | 86.0 | 1528.2 | 66.2 | 66.4 | 60.6 | 67.0 | 31.5  | 
 |  LLaVA-1.5[^1] | LVIS-Instrcut4V | 13B | full_ft-1e | [LVIS-Instruct4v-13b](https://huggingface.co/X2FD/LVIS-Instruct4v-13b) | 80.1 | 63.8 | 51.4 | 73.0 | 62.1 |  85.3 | 1572.0 | 67.8 | 68.2 | 62.5 | 76.7 | 40.2 |
 |  LLaVA-1.5 | LVIS-Instrcut4V + LLaVA-Instruct | 13B | full_ft-1e | [LVIS-Instruct4v-13b](https://huggingface.co/X2FD/LVIS-Instruct4v-13b) | 80.7 | 63.6 |57.2 | 74.2 | 62.5 | 86.0 | 1574.9 | 68.0 | 67.4 | 61.6 | 71.3 | 37.4

[^1]: We find TextQA is sensitive to the beam number, and for 13B models, we use beam = 3.

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
