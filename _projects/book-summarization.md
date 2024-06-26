---
layout: project
title: Book summarization
---

# 📚 Book summarization with LLMs

## 🤔 Why do we care about this problem?

As the context windows of LLMs scale up to [millions of tokens](https://blog.google/technology/ai/google-gemini-next-generation-model-february-2024/), book-length summarization becomes an increasingly relevant problem. Most prior work on summarization has focused on documents of a few hundred or thousand tokens, making book summarization a largely unexplored area of research. Our work at the [UMass Amherst NLP group](https://nlp.cs.umass.edu/) includes completed, ongoing, and future projects focused on the book summarization task.

## ✅ Completed projects

### 📖 *BooookScore: A systematic exploration of book-length summarization in the era of LLMs* [[paper](https://arxiv.org/pdf/2310.00785) | [code & data](https://github.com/lilakk/BooookScore)]

Authors 👉 [Yapei Chang](https://lilakk.github.io/), [Kyle Lo](https://kyleclo.com/), [Tanya Goyal](https://tagoyal.github.io/), [Mohit Iyyer](https://people.cs.umass.edu/~miyyer/)

![coherence](assets/img/coherence.png)

In this work, we explore coherence evaluation in the book summarization setup. After collecting newly published books unlikely to have been seen by LLMs during training, we adopt a finegrained human annotation protocol to evaluate book summaries generated by models like GPT-4 and Mixtral. Annotators are asked to read through a summary, highlight confusing spans, and ask clarification questions. We subsequently derive an error taxonomy based on these annotations, and find that omission is the most common error type. Motivated by the high costs associated with human evaluation, we propose an automatic evaluation metric, BooookScore, where we use GPT-4 to obtain finegrained annotations and compute a coherence score as the percentage of sentences that are error-free in a summary. This metric is found to align well with human judgment.

### 🦄 *FABLES: Evaluating faithfulness and content selection in book-length summarization* [[paper](https://arxiv.org/pdf/2404.01261) | [code & data](https://github.com/mungg/FABLES)]

Authors 👉 [Yekyung Kim](https://mungg.github.io/), [Yapei Chang](https://lilakk.github.io/), [Marzena Karpinska](https://marzenakrp.github.io/), [Aparna Garimella](https://research.adobe.com/person/aparna-garimella/), [Varun Manjunatha](https://research.adobe.com/person/varun-manjunatha/), [Kyle Lo](https://kyleclo.com/), [Tanya Goyal](https://tagoyal.github.io/), [Mohit Iyyer](https://people.cs.umass.edu/~miyyer/)

![faithfulness](assets/img/faithfulness.png)

A major limitation of BooookScore is that it only focuses on coherence. In FABLES, we aim to fill this gap by conducting a human evaluation of faithfulness and content selection on LLM-generated book summaries. After collecting a set of newly published books, we obtain LLM summaries, extract claims from these summaries with GPT-4, then hire annotators who have already read these books to evaluate the faithfulness of the claims while citing evidence from the books. Our error analysis suggests that most unfaithful claims are related to events or states of characters and relationships. We further experiment with automatically evaluating faithfulness using LLMs, but find that they struggle to identify unfaithful claims. As we observe from annotators' high-level comments, verifying unfaithful claims is also a hard task for humans since it often is less direct and involves aggregating evidence from multiple parts of the book. Apart from faithfulness, we also analyze how well summaries cover the content of the books. Insights from annotators' comments reveal that important events, details, and themes are frequently omitted by all LLMs.

## ✨ Work in progress

- *Automatic claim verification with LLMs*: We delve deeper into automatically evaluating the faithfulness of LLM-generated book summaries by asking LLMs to verify claims extracted from summaries.

- *Summarizing series of books*: Instead of standalone books, we scale up to series of books to better utilize and test LLMs' long context windows.

## 👀 Exciting future directions

- *Query-focused summarization*: Given a query related to a book, how well can LLMs write a summary given access to the entire book?
