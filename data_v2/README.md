# InstructWild Data v2

We release a large set of user-based high quality instructions as our InstructWild v2. All insturctions are collected on the web without using GPT to generate instructions. We have 4 different files:

- user_1.jsonl: 429 instructions from Twitter, which is actually the same set of instructions as our Instruction v1. However, we provide more diverse labels like instruction_type and special_tag.
- user_2.jsonl: 248 instructions from [Cookup.AI](https://cookup.ai/chatgpt/usecases/)
- user_3.jsonl: 201 instructions from [GitHub](https://prompts.chat/)
- user_4.jsonl: 110031 instructions from Discord

We also release the code to filter the Discord instructions. We finetuned DistillBERT to extract instructions from the raw discord conversations.

Thanks Kabear and Mahir for the great contributions!
