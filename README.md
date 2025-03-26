# text_summarisation

## **Project Objective**

To fine-tune a BART model to automatically generate concise and coherent summaries of chat-based conversations using the SAMSum dataset.

## **Dataset**

* Name: SAMSum

* Source: Hugging Face Datasets

* Description: A collection of ~16k messenger-style conversations, each paired with a human-written summary.

## **Tools & Technologies**

* Model: facebook/bart-large-cnn

## **Libraries:**

* transformers

* datasets

* evaluate

* pandas

* torch


## **Methodology**

* Load Dataset: A reduced portion of the SAMSum dataset (200 training samples, 50 validation samples) was used to reduce training time.

* Preprocessing: Tokenized dialogues and summaries using BART tokenizer with max lengths of 512 (input) and 128 (target).

* Fine-tuning:

Trained for 2 epochs

Batch size of 4

Learning rate: 2e-5

* Evaluation:

Used ROUGE scores to evaluate output summaries

Also included manual test examples to assess model fluency

## **Results**

### ROUGE Scores (Fine-tuned BART)

* ROUGE-1: 0.4446

* ROUGE-2: 0.2088

* ROUGE-L: 0.3478

* ROUGE-Lsum: 0.3478

## **Manual Test Output Examples**

Input: "John: Are you free tomorrow? Sarah: Yes, after 3 PM..."
Summary: "Sarah is free tomorrow after 3 PM. John will meet with Sarah at 4 PM."

## **Target Audience**

This project is aimed at individuals and organizations that frequently handle informal, chat-based communication and need efficient summarization tools.

### Examples include:

* Customer support and call center teams

* Collaboration tool users (Slack, Teams, Discord)

* Journalists and content creators

* NLP developers and researchers

* Busy professionals and students

## **Strengths**

* Quick and efficient fine-tuning

* Fluent and coherent summaries

* Strong results on small dataset

## **Limitations**

* Minor factual inconsistencies

* ROUGE-2 could be improved

## **Recommendations**

* Train on more samples (1000+)

* Increase epochs to 3–5 to improve results

* Add factual consistency checks

* Test on more varied conversation types



