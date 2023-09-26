# News Document & Token Classification

### Document Classification

- Two methods are employed for classification: Naive Bayes and Transformers. 
- Each method’s results are evaluated for effectiveness.
- In the Naive Bayes approach, the TF-IDF technique is used to vectorize the data.
- For Transformer method, the ‘SajjadAyoubi/distil-bigbird-fa-zwnj’ model is utilized to tokenize the data.

### Token Classification (HMM)

- The model takes a text and a question as inputs and provides an answer extracted directly from the text.
- Use ‘SajjadAyoubi/persian_qa’ dataset.
- Labels are created from the start and end indices of the answer within the text. These labels are vectorized using the TF-IDF technique.

### Token Classification (Tranformers)

- The model is designed to accept a text and a question, and it provides an answer derived directly from the input text.
- Use 'SajjadAyoubi/persian_qa' dataset.
- Labels are generated from the start and end indices of the answer within the text. These labels are then vectorized using a pretrained model from HuggingFace, which is also used to predict the answers to the corresponding questions.


### NER
- It involves extracting information to identify and categorize named entities in unstructured text into predefined categories such as Person (PER), Location (LOC), Main location (mainLoc), Event (EVE), Date (DAT), Organization (ORG), Time (TIM), Facility (FAC), Money (MON), Percent (PCT), and Product (PRO).
- The dataset is then preprocessed and the dataset labels are translated into model labels.
- The model is trained using the prepared data.
- The final step involves checking the true and predicted outputs and evaluating their performance.
