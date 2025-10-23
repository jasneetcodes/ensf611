# Machine Learning


## What is machine learning?

Powerful tool for data analysis

Need to understand the concepts of:
- bias and variance
- overfitting and underfitting
- and more...

- A subset of artificial intelligence
- Used to build mathematical models of data
- Used to 'learn' the pattern of the data to create the appropriate mathematical model for prediction, classification etc.



## AI vs ML vs DL

AI
- helpds build system that automatically sorts emails into Inbox Spam or Promotions, like a human would

ML
- System is trained on thousands of labeled emails
- It learns what spam usually looks like
- Over time, it gets better at predicting whether new emails are spam

DL
- Goes beyond surface level features
- Analyze email writing tone, embedded images, sender behavior, fake branding tricks
- Helps detect advnaced phishing attacks that are hard to catch with simple ML


## Different types of machine learning

Supervised Learning
- Regression and classification

Unsupervised Learning
- Clustering and Dimensionality Reduction

Semi Supervised Learning

Reinforcement Learning

## What is supervised learning?

Inputs -> Relationship -> Outputs

Want to figure out the relationship part

Learns from examples with correct answers (labeled data)

Algorithm learns to map inputs to outputs by studying many input-output pairs

Ex. Email spam detection, image recognization 


## Training and testing your model

Data is split into Training and Testing Sets

Training set is used to train the selected model, find the relationship between the input and output

Testing set is used to test if the relationship is correct, by comparing the produced output to the expected output.

**Selection of data is very important


## What is Unsupervised Learning?

Inputs -> Relationship -> Outputs
known        unknown       unknown


It finds hidden patterns in data. Explores structure, groups or relationships
No labels or outputs

Ex. Data clustering, anomaly detection, recommendation system

## What is Semi Supervised Learning?

Inputs -> Relationship -> Outputs
known       unknown         partially unknown

Uses small amount of labeled data and large amount of UNLABELED data. Model learns from the labels and patterns in unlabeled data

Like learning with hints

Ex. speech recognition

## What is Reinforcement Learning?

Computer takes action -> System responds -> Outcome of action -> Computer makes changes to strategy -> LOOP

Learning through interaction with an environment.

Agent takes acions and receives either REWARD or PENALTY, and learns to maximize long term rewards

Ex. Chess, Robot navigation