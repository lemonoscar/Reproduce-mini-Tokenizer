# Basic BPE Tokenizer

这是一个基于Andrej Karpathy的[minbpe练习](https://github.com/karpathy/minbpe/tree/master)实现的简单BPE（Byte Pair Encoding）分词器。本仓库旨在帮助初学者理解BPE算法的核心思想，并提供一个基础但完整的实现，适用于自然语言处理任务的文本预处理。

## 项目简介

BPE是一种常用的子词分词方法，广泛应用于现代NLP模型（如BERT、GPT等）。它通过迭代合并出现频率最高的字符对，逐步构建词表，最终将文本分割为子词单元。本项目实现了一个基础版本的BPE分词器，支持训练和分词功能。

### 功能特点
- **训练词表**：从输入文本中学习BPE合并规则，生成词表。
- **文本分词**：将新文本按照训练好的词表进行分词。
- **轻量实现**：代码简洁，易于理解和扩展。
- **基于字符**：支持任意语言的字符级输入。

## 安装

### 环境要求
- Python 3.6+
- 无需额外依赖库


## 使用方法

### 1. 训练BPE模型
运行以下命令，从文本文件中训练BPE词表：
```bash
python tokenizer.py --train --input input.txt --num_merges 1000 --output vocab.json
```
- `--input`：输入文本文件路径。
- `--num_merges`：指定合并次数（即词表大小）。
- `--output`：保存词表和合并规则的文件。



## 贡献
欢迎提交Issue或Pull Request！如果有改进建议或发现bug，请随时联系。

## 致谢
本项目受Andrej Karpathy的[minbpe](https://github.com/karpathy/minbpe)启发，感谢他提供的优秀教学资源。
