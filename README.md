# Implementing-Many-to-Many-RNN-for-English-to-Urdu-Language-Translation-and-Exploring-Its-Limitations

Title: Implementing Many-to-Many RNN for English-to-Urdu Language
Translation and Exploring Its Limitations
Part 1: Many-to-Many Recurrent Neural Network (RNN) Implementation
Objective:
Implement a many-to-many RNN model for English-to-Urdu language translation using a
publicly available dataset.
Public Dataset:
Use the parallel-corpus.xlsx parallel corpus for English-Urdu translation. The dataset includes
parallel sentences in English and Urdu, which can be used for training and evaluation.
Tasks:
1. Data Preparation:
o Download the parallel-corpus.xlsx dataset.
o Preprocess your data in both English and Urdu.
o Split the dataset into training, validation, and test sets.
2. Model Architecture:
o Build an RNN-based many-to-many architecture using TensorFlow or PyTorch.
o Train the model for English-to-Urdu translation.
3. Evaluation:
o Evaluate the model using appropriate metrics like BLEU score or accuracy.
o Provide example translations for a few test sequences.
Instructions:
• Submission will be Online. Submit python file(s) with single word file containing report
and code with Screenshots of running codes.
• Late submissions are not allowed.
• Solve all the questions in the given order.
• Write the programs with clarity and add comments where necessary.
• Each question carries 10 marks.
• The evaluation will be viva based with binary marking.
• This is a group assignment. Maximum 2 persons are allowed.

CS-4063 Natural Language Processing

2

Part 2: Reporting the Limitations of RNNs
Objective:
Discuss the limitations of RNNs in the context of language translation.
Tasks:
1. Limitations to Discuss:
o The challenge of handling long sequences due to exploding/vanishing gradients.
o Difficulty in capturing long-term dependencies between words, especially for
languages with complex grammatical structures like Urdu.
o Poor performance on large datasets with complex language pairs.
o Show examples of each scenario generated from dataset.






Part 2: Limitations of RNN

1. Exploding/Vanishing Gradients in Long Sequences
• Limitation: RNNs struggle with long sequences because gradients either become too
large (exploding) or too small (vanishing) during backpropagation. This makes it hard
to capture dependencies between distant words in a sentence.
• Example:
o Input (English): "The meeting, which was delayed due to heavy rain, finally
started after two hours."
o Translation (Urdu): The RNN may fail to connect the subject "meeting" with
"started" at the end of the sentence, producing an incomplete or inaccurate
translation.
یئ بارش یک وجہ ےس دیر ، " :Output o

ہوگ آخر کار دو

subject Missing " (گھنٹ ےک بعد۔
"meeting")

2. Difficulty Capturing Long-Term Dependencies
• Limitation: RNNs face challenges in maintaining context over long sequences,
especially for complex languages like Urdu, where grammatical structure and word
agreement depend on distant elements.
• Example:
o Input (English): "She told me that her brother, who works in a bank, is getting
married next month."
o Translation (Urdu): The model might struggle to connect "brother" to the
correct pronouns and verbs, resulting in a translation error.

ی اس کا ، " :Output o
ےہ بھائ جو بینک م ی کام کرتا ،
اگےل
ےہ مہین شادی کر رہا ۔

" (Grammatical

errors or missing context)
3. Poor Performance on Large Datasets
• Limitation: RNNs often perform poorly on large datasets involving complex language
pairs like English-Urdu due to their limited ability to parallelize, leading to inefficient
training and slow convergence.
• Example:
o For a dataset with large sentences, the RNN’s BLEU score remains low,
reflecting poor generalization to unseen data.
o BLEU Score: ~6.30 (as shown in your results)
o This score indicates that the model is generating translations far from the
reference translations, especially when trained on a large and diverse dataset.

4. Complex Grammatical Structures
• Limitation: Urdu has rich inflections, gendered words, and a more flexible word
order than English. RNNs may misinterpret the structure, leading to inaccurate
translations.
• Example:
o Input (English): "The teacher praised the students who performed well."
o Translation (Urdu): RNN may confuse the subject and object or produce the
wrong gender agreement.
o Output: " اساتذہ
ن ان طلباء یک تعریف یک جو اچھا

دکھایا۔ کارکردیک) " Gender or tense
mismatch)
Suggestions to Improve:

• To mitigate these limitations, using more advanced architectures like Long Short-
Term Memory (LSTM) or Transformer models can be more effective.
