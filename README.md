# Instruction in the Wild: A User-based Instruction Dataset

## News

We release InstructWild v2 under `data v2` dir, which includes over 110K high-quailty user-based instructions. We did not use self-instruct to generate any instructions. We also label a subset of these instructions with instruction type and speical tag. Please see [README](https://github.com/XueFuzhao/InstructionWild/blob/main/data_v2/README.md) for details.

## Introduction

Instruction Tuning is a key component of ChatGPT. OpenAI used their user-based Instruction dataset, but unfortunately, this dataset is not open-sourced. [Self-Instruct](https://github.com/yizhongw/self-instruct) released a small instruction dataset including 175 instructions written by human labors. [Standford Alpaca Team](https://github.com/tatsu-lab/stanford_alpaca) generated 52K instructions by `text-davinci-003` model based on the the 175 seed instructions above.

This project targets on a larger and more diverse instruction dataset. To this end, we collected (110K in v2 dataset, 429 in v1 dataset) instructions from ChatGPT usage sharing and released both English and Chinese versions. We found these instructions are very diverse. We follow [Alpaca](https://github.com/tatsu-lab/stanford_alpaca) to generate 52K instructions and their responses. All data can be found in `data` and `data v2` dir.

Note: This is an ongoing project. We are still collecting and improving our data. We release this dataset as early as possible to speedup our LLM research. We will also release a whitepaper soon.

## Data Release

Our dataset use the same format as [Alpaca](https://github.com/tatsu-lab/stanford_alpaca) for fast and easy usage. Our instructions have no input field.

## Data Collection (InsturctWild v1)

![data_collection](./imgs/data-collect.png)

We scrapt over 700 noisy instructions from Twitter and filter out noisy instructions. We then pick 429 clean insturctions to ensure the high quality.

We use a similar method as Alpaca to collect instructions. However, we do not need outputs for instructions thus avoid human involvement. The prompts generated are more diverse and covers more topics compared to the Alpaca's.

We provide 5 prompts as examples for generating new instructions from OpenAI API. After collecting prompts, we collect responses of these instructions from OpenAI API. The English and Chinese datasets are generated seperately. In total, 880$ are spent to collect the dataset. There are 52K instructions for English (around 24M tokens) and 52K instructions for Chinese.

## How Good is InstructWild?

[Colossal AI](https://colossalai.org/) used our model to train the [ColossalChat](https://github.com/hpcaitech/ColossalAI/tree/main/applications/Chat) model. The ColossalChat-7B (only after stage-1) combines the original alpaca dataset and our dataset. We compare the ColossalChat-7B with Alpaca-7B to see what improvement our dataset brings.

It is difficult to evaluate Chatbot. We human-evaluate several examples under different categories of instructions. Our main findings are:

### Pros

- Our new dataset improves the model's ability in **Generation, Open QA, and Mind Storm instructions**. This corresponds to our data collection process. Our data is collected from Twitter, where users tend to share their interesting prompts of mostly generation, open QA, and mind-storm types.

### Limitations for LLaMA-finetuned models

- Both Alpaca and ColossalChat are based on LLaMA. It is hard to compensate for the missing knowledge in the pre-training stage.
- Lack of counting ability: Cannot count the number of items in a list.
- Lack of Logics (reasoning and calculation).
- Tend to repeat the last sentence (fail to produce the end token).
- Poor multilingual results: LLaMA is mainly trained on English datasets (Generation performs better than QA).

### Limitations of dataset

- Lack of summarization ability: No such instructions in finetune datasets.
- Lack of multi-turn chat and role-playing: No such instructions in finetune datasets
- Lack of self-recognition: No such instructions in finetune datasets
- Lack of Safety:
  - When the input contains fake facts, the model makes up false facts and explanations.
  - Cannot abide by OpenAI's policy: When generating prompts from OpenAI API, it always abides by its policy. So no violation case is in the datasets.

## Detailed Comparison

See [**HERE**](./comparison.md) for detailed comparison.

## TODO

- [x] Dataset v1
- [ ] Data Generation Code
- [x] Fine-grained Labeling
- [x] Larger Dataset (Dataset v2)

## Authors

This dataset is collected and cleaned by the following authors:

- [Fuzhao Xue](https://xuefuzhao.github.io/)
- [Zangwei Zheng](https://zhengzangw.github.io/)
- [Kabir Jain](https://github.com/ka-bear)
- [Mahir Hitesh Shah](https://github.com/RottenLemons)

All authors are advised by [Prof. Yang You](https://www.comp.nus.edu.sg/~youy/).

We also acknowledge the valuable suggestions from [Prof. Aixin Sun](https://personal.ntu.edu.sg/axsun/), [Dr. Tom Young](https://tomyoung903.github.io/).

## Citation

Please cite the repo if you use the data or code in this repo.

```bibtex
@misc{instructionwild,
  author = {Fuzhao Xue, Kabir Jain, Mahir Hitesh Shah, Zangwei Zheng and Yang You },
  title = {Instruction in the Wild: A User-based Instruction Dataset},
  year = {2023},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/XueFuzhao/InstructionWild}},
}
```
