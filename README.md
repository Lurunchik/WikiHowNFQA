#  WikiHowQA: A Comprehensive Benchmark for \\ Multi-Document Non-Factoid Question Answering

This repository is for the paper "WikiHowQA: A Comprehensive Benchmark for Multi-Document Non-Factoid Question Answering" presented at ACL 2023. 
The paper introduces WikiHowNFQA, a unique collection of 'how-to' content from WikiHow, transformed into a rich dataset featuring 11,746 human-authored answers
and 74,527 supporting documents. 

The dataset is designed for researchers and presents a unique opportunity to tackle the challenges 
of creating comprehensive answers from multiple documents and grounding those answers in the real-world context provided by the supporting documents.

## Dataset Structure

The dataset is structured as follows:

- `article_id`: The ID of the WikiHow article from which the question and answer were extracted.
- `question`: The question.
- `answer`: The answer to the question.
- `related_document_urls_wayback_snapshots`: A list of URLs to documents related to the question and answer.
- `split`: The dataset split that this example belongs to (train, validation, or test).
- `cluster`: The cluster ID that this example belongs to.

## Data Loading

You can load the data using the following Python code:

```python
from datasets import load_dataset

dataset = load_dataset('WikiHowNFQA.jsonl')
```

## Download the Dataset

The WikiHowQA dataset is divided into two parts:

1. **Main Part**: This part contains the questions, answers, and URLs to related documents. It is publicly available and can be downloaded from the Hugging Face Datasets platform [here](https://huggingface.co/datasets/Lurunchik/WikiHowNFQA). You can explore it and load this part of the dataset using the Hugging Face `datasets` library as follows:

    ```python
    from datasets import load_dataset
    dataset = load_dataset('wikiHowNFQA')
    ```

2. **Document Content Part**: This part contains the parsed HTML content of the related documents. To access this part of the dataset, you need to sign a Data Transfer Agreement with RMIT University. You can request access to this part of the dataset on the WikiHowQA website [here](https://lurunchik.github.io/WikiHowQA/).

## Paper

The WikiHowQA dataset was introduced in our paper titled "WikiHowQA: A Comprehensive Benchmark for Multi-Document Non-Factoid Question Answering", which was presented at the 61st Conference of the Association for Computational Linguistics (ACL) in 2023.

In the paper, we discuss the creation of the WikiHowQA dataset, its structure, and its potential uses. We also present a unique human evaluation framework that smartly employs highlighted relevant supporting passages to circumvent common challenges in the field.

You can read the full paper [here](https://lurunchik.github.io/WikiHowQA/data/ACL_MD_NFQA_dataset.pdf).

If you use the WikiHowQA dataset in your research, please cite our paper:

```bibtex
@inproceedings{bolotova2023wikihowqa,
      title={WikiHowQA: A Comprehensive Benchmark for Multi-Document Non-Factoid Question Answering}, 
      author={Bolotova, Valeriia and Blinov, Vladislav and Filippova, Sofya and Scholer, Falk and Sanderson, Mark},
      booktitle="Proceedings of the 61th Conference of the Association for Computational Linguistics",
      year={2023}
}
```
