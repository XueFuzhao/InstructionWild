# Comparison between Alpaca and ColossalChat

The [Alpaca-7B](https://github.com/tatsu-lab) is trained on 52k instructions. [ColossalChat-7B](https://github.com/hpcaitech/ColossalAI/tree/main/applications/Chat) (stage 1) is trained with the same supervised learning. It is trained on 52k instructions from Alpaca and our 52k instructions, plus 52k our Chinese dataset.

The comparison is given based on different categories of instructions. The colorful results are the ColossalChat-7B results and the black-and-white results are the Alpaca-7B results.

## Generation

### Email

ColossalChat **[Better]**:

![email](./imgs/email-1.png)

Alpaca: it wrongly thinks the Ph.D. program is in the professor's group.

![email](./imgs/email-2.png)

### Code 1

ColossalChat **[Better]**:

![code](./imgs/code-1.png)

Alpaca: it fails to implement quick-sort.

![code](./imgs/code-2.png)

### Regex

ColossalChat **[Better]**:

![code](./imgs/regex-1.png)

Alpaca: it fails to give a complete regex.

![code](./imgs/regex-2.png)

### TeX

### Outline

### Poem

## Open QA

## Mind Storm

## Chat

## Understanding

## Logics

## Role-playing

## Safety

## Chinese 中文
