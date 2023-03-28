# Instruction in the Wild: A User-based Instruction Dataset


## Introduction

Instruction Tuning is a key component of ChatGPT. OpenAI used their user-based Instruction dataset, but unfortunately, this dataset is not open-sourced. [Self-Instruct](https://github.com/yizhongw/self-instruct) released a small instruction dataset including 175 instructions written by human labors. [Standford Alpaca Team](https://github.com/tatsu-lab/stanford_alpaca) generated 52K instructions by `text-davinci-003` model based on the the 175 seed instructions above. 

This project targets on a larger and more diverse instruction dataset. To this end, we collected 429 instructions from ChatGPT usage screenshots and released both English and Chinese versions. We found these instructions are very diverse even if the scale is still small. We follow [Alpaca](https://github.com/tatsu-lab/stanford_alpaca) to generate 52K instructions and their responses. All data can be found in `data` dir.

Note: This is an ongoing project. We are still collecting and improving our data. We release this dataset as early as possible to speedup our LLM research. We will also release a whitepaper soon.

## Data Release

Our dataset use the same format as [Alpaca](https://github.com/tatsu-lab/stanford_alpaca) for fast and easy usage.
TODO(Zangwei)


## Data Collection

We scrapt over 700 noisy instructions from Twitter and filter out noisy instructions. We then pick 429 clean insturctions to ensure the high quality.
TODO(Zangwei)

## How Good is InstructWild?

[Colossal AI](https://colossalai.org/) used our model to train.


## TODO

- [x] Dataset v1
- [ ] Data Generation Code
- [ ] Fine-grained Labeling
- [ ] Larger Dataset (Dataset v2)



## Authors

This dataset is collected and cleaned by the following authors:

- [Fuzhao Xue](https://xuefuzhao.github.io/)
- [Zangwei Zheng](https://zhengzangw.github.io/)

Both authors are advised by [Prof. Yang You](https://www.comp.nus.edu.sg/~youy/). 

We also acknowledge the valuable suggestions from [Prof. Aixin Sun](https://personal.ntu.edu.sg/axsun/), [Dr. Tom Young](https://tomyoung903.github.io/).

## Citation

Please cite the repo if you use the data or code in this repo.

```
@misc{instructionwild,
  author = {Fuzhao Xue and Zangwei Zheng and Yang You },
  title = {Instruction in the Wild: A User-based Instruction Dataset},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/XueFuzhao/InstructionWild}},
}
```
