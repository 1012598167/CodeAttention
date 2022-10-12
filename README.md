# CAT-probing: A Metric-based Approach to Interpret How Pre-trained Models for Programming Language Attend Code Structure

## Updates

- 2022/10/06: Release the paper of CAT-probing, check out our [paper](https://arxiv.org/abs/xxxx.yyyy). 👏
- 2022/10/06: CAT-probing is accepted by **Findings of EMNLP 2022** 🎉

## Introduction

**TBD**

More details are provided in our EMNLP22 paper and our arXiv paper [CAT-probing: A Metric-based Approach to Interpret How Pre-trained Models for Programming Language Attend Code Structure](CAT-probing: A Metric-based Approach to Interpret How Pre-trained Models for Programming Language Attend Code Structure).

## Environment

**to be continued requirements**

**add coauthor github**

```bash
conda create --name cat python=3.7
conda activate cat
pip install transformers==4.1.1
pip install pytorch=1.5.1
pip install datasets
pip install sklearn
git clone https://github.com/nchen909/CodeAttention
cd CodeAttention
```

## Using CAT-probing

### Preparing Data

The dataset we use comes from [CodeSearchNet](https://github.com/microsoft/CodeXGLUE/tree/main/Code-Text/code-to-text) and you can download from [google drive link].**to be continued**

## Citation

**to be continued**

## Train

```bash
export MODEL_NAME=
export TASK="summarize"
export SUB_TASK=
bash run.sh $MODEL_NAME $TASK $SUB_TASK
```

  `MODEL_NAME` can be any one of `["roberta", "codebert", "graphcodebert", "unixcoder"]`.

  `SUB_TASK` can be any one of `["go", "java", "javascript", "python"]`.

## Probing

```bash
export MODEL_NAME=
export TASK="summarize"
export SUB_TASK=
export LAYER_NUM=
bash run_att.sh $MODEL_NAME $TASK $SUB_TASK $LAYER_NUM
```

`MODEL_NAME` can be any one of `["roberta", "codebert", "graphcodebert", "unixcoder"]`.

`SUB_TASK` can be any one of `["go", "java", "javascript", "python"]`.

`LAYER_NUM` can be any one of `[0-11]` or `-1` (`11` refers to the last layer,  `-1` refers to all `[0-11]` layers).

## Visualization

Visualization results can be found in `att-vis-notebook` folder.


If you use this code or UniXcoder, please consider citing us.👇

```
@article{TBD,
  title={CAT-probing: A Metric-based Approach to Interpret How Pre-trained Models for Programming Language Attend Code Structure},
  author={Chen, Nuo and Sun, Qiushi and Zhu, Renyu and Xiang, Li and Xuesong, Lu and Ming, Gao},
  journal={arXiv preprint arXiv:TBD},
  year={2022}
}
```
