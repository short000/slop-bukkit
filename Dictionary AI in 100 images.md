# Activation Function
An activation function is a mathematical "gate" inside a neuron in a neural network. After the neuron sums up all its inputs, the activation function decides what the output signal should be. Its primary role is to introduce non-linearity into the network, which allows the model to learn complex, non-linear patterns in the data. Without it, a neural network would just be a simple linear regression model.

For example, the **ReLU (Rectified Linear Unit)** function is very common. If the input to the ReLU function is positive, it outputs the same value. If the input is negative, it outputs zero. This simple rule helps the network learn efficiently by "activating" only certain neurons.

***
## Formal Definition
Common activation functions include:
* **Sigmoid:** $\sigma(x) = \frac{1}{1 + e^{-x}}$
    * Squeezes any real number into the range (0, 1). Used in older models or for binary classification output layers.
* **Hyperbolic Tangent (tanh):** $\tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
    * Squeezes any real number into the range (-1, 1). It is zero-centered, which can help with optimization.
* **Rectified Linear Unit (ReLU):** $f(x) = \max(0, x)$
    * Outputs the input if it's positive, and 0 otherwise. It is computationally efficient and helps mitigate the vanishing gradient problem.

---
# Algorithm
An algorithm is a finite sequence of well-defined, computer-implementable instructions, typically to solve a class of problems or to perform a computation. It's a step-by-step recipe that takes an input, follows a series of explicit steps, and produces an output.

For example, a simple algorithm for finding the largest number in a list is:
1.  Assume the first number in the list is the largest.
2.  Go through the rest of the numbers one by one.
3.  If you find a number that is larger than the one you currently assume is the largest, replace it.
4.  After checking all the numbers, the number you have is the largest.

---
# ANN (Artificial Neural Network)
An Artificial Neural Network is a computational model inspired by the structure and function of the human brain. It consists of interconnected nodes, called neurons, organized in layers. Each connection has a weight that is adjusted during training. The network learns by processing examples, adjusting the weights to minimize the difference between its predictions and the actual outcomes.

For example, an ANN can be trained to recognize handwritten digits. It would be fed thousands of images of digits (0-9), and for each one, it would try to guess the digit. If it guesses wrong, it adjusts its internal weights using an algorithm like backpropagation until its guesses become highly accurate.

---
# Artificial Intelligence
Artificial Intelligence (AI) is a broad field of computer science dedicated to creating machines that can perform tasks that typically require human intelligence. This includes capabilities like learning from experience, reasoning, solving problems, understanding language, and perceiving the environment. AI encompasses everything from simple rule-based systems to complex deep learning models.

For example, when you use a navigation app like Google Maps or Waze, the AI is analyzing real-time traffic data, road conditions, and historical patterns to find the fastest route to your destination, a complex problem-solving task.

---
# Attention
The attention mechanism is a technique used in neural networks, particularly for sequential data like text, that allows the model to dynamically focus on the most relevant parts of the input when producing an output. Instead of treating all input words equally, it assigns different "attention scores" to each word, amplifying the importance of some and diminishing others based on the current context.

For example, when translating the sentence "The cat sat on the mat, it was happy," the attention mechanism would help the model understand that "it" refers to "the cat" and not "the mat" by placing a higher attention score on "cat" when translating the word "it."

***
## Formal Definition
The most common form is Scaled Dot-Product Attention, defined as:

$$
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
$$

where:
* $Q$ (Query): The representation of the current word we are focusing on.
* $K$ (Keys): The representations of all the words in the sequence that we can pay attention to.
* $V$ (Values): The actual representations of the words.
* $d_k$: The dimension of the keys, used for scaling to prevent gradients from becoming too small.

---
# Auto ML (Automated Machine Learning)
AutoML is the process of automating the time-consuming, iterative tasks of applying machine learning to real-world problems. It automates the end-to-end pipeline, including data preprocessing, feature engineering, model selection, hyperparameter tuning, and model deployment. The goal is to make machine learning more accessible to non-experts and more efficient for experts.

For example, a business analyst could use an AutoML platform to build a sales forecasting model. They would upload their historical sales data, and the AutoML system would automatically test hundreds of different models (like linear regression, random forests, etc.) and configurations to find and deploy the one that produces the most accurate forecasts.

---
# Autoencoder
An autoencoder is a type of unsupervised neural network that learns to create a compressed representation (encoding) of its input data and then reconstruct the original data from that compressed version. It consists of two parts: an **encoder** that compresses the data into a lower-dimensional "latent space," and a **decoder** that reconstructs the data from this latent space. The network is trained to minimize the difference between the original input and the reconstructed output.

For example, autoencoders are often used for image denoising. The model is trained on noisy images as input and clean images as the desired output. The encoder learns to capture the essential features of the image in the latent space, ignoring the noise, allowing the decoder to reconstruct a clean version.

---
# Backpropagation
Backpropagation is the core algorithm used to train artificial neural networks. It works by calculating the error (or loss) of the network's prediction and then propagating this error backward from the output layer to the input layer. As the error propagates, it calculates the gradient (the "slope" of the error) for each weight in the network. These gradients are then used by an optimization algorithm, like gradient descent, to update the weights in the direction that will minimize the error.

For example, if a network predicts a cat is a dog, the loss will be high. Backpropagation calculates how much each weight and bias contributed to that error. It then tells the optimizer how to adjust those weights—"tweak this one down a bit, that one up a bit"—to make the network more likely to predict "cat" next time it sees a similar image.

---
# Bag of Words (BoW) Model
The Bag of Words model is a simple way to represent text data for machine learning algorithms. It describes the occurrence of words within a document, completely ignoring grammar and word order but keeping track of frequency. It's called a "bag" of words because it treats the text as an unordered collection of words, like words jumbled in a bag.

For example, the sentence "The cat sat on the mat" would be represented as a dictionary of word counts:
`{"the": 2, "cat": 1, "sat": 1, "on": 1, "mat": 1}`.
This numerical representation can then be used as input for a machine learning model.

---
# Bias
In machine learning, bias is a type of error that occurs when a model is too simple to capture the underlying patterns in the data. A high-bias model makes overly simplistic assumptions, leading it to consistently miss the relevant relations between features and outputs. This results in **underfitting**, where the model performs poorly on both the training data and new, unseen data.

For example, trying to model a complex, curved relationship in data (like the relationship between a car's speed and its fuel efficiency) using a simple straight line (linear regression) would result in a high-bias model. The line would be a poor fit for the data everywhere.

---
# Classification
Classification is a supervised learning task where the goal is to predict a categorical class label. The model is trained on a dataset of inputs with their corresponding correct labels and learns to assign new, unseen inputs to one of the predefined categories.

For example, an email service uses a classification model to determine if an incoming email is `"spam"` or `"not spam"`. The model is trained on millions of emails that have already been labeled, and it learns the patterns associated with each category to classify new emails automatically.

---
# Clustering
Clustering is an unsupervised learning technique used to group a set of data points in such a way that points in the same group (called a cluster) are more similar to each other than to those in other clusters. The goal is to discover the natural groupings in the data without any predefined labels.

For example, a marketing team could use clustering to segment its customer base. By clustering customers based on their purchasing habits, age, and location, the team can discover distinct groups (e.g., "young urban professionals," "suburban families") and tailor marketing campaigns specifically for each group.

---
# CNN (Convolutional Neural Network)
A Convolutional Neural Network is a type of deep learning model specifically designed for processing data with a grid-like topology, such as an image. CNNs use special layers called convolutional layers that apply filters (or kernels) across the input image to automatically learn and detect features, such as edges, textures, and shapes. These layers are arranged in a hierarchy, allowing the network to learn simple features in the early layers and combine them to detect more complex objects in the deeper layers.

For example, in an image recognition task, the first convolutional layer might learn to detect simple edges. The next layer might combine these edges to detect corners and shapes. A deeper layer might combine those shapes to detect parts of an object, like an eye or a wheel, until the final layer can identify the entire object, like a face or a car.

---
# Collaborative Filtering
Collaborative filtering is a technique used by recommendation systems to make automatic predictions about the interests of a user by collecting preferences from many users. The underlying assumption is that if person A has the same opinion as person B on an issue, A is more likely to have B's opinion on a different issue than that of a randomly chosen person.

For example, a movie streaming service uses collaborative filtering to recommend movies. It looks at the movies you have liked and finds other users who have liked those same movies. It then looks at other movies those similar users have liked that you *haven't* seen and recommends them to you.

---
# Confusion Matrix
A confusion matrix is a table used to evaluate the performance of a classification model. It provides a detailed breakdown of how many predictions were correct and what kinds of errors the model made. The matrix compares the actual true values with the predicted values from the model.

For a binary classification problem, the matrix has four cells:
* **True Positives (TP):** The model correctly predicted the positive class. (e.g., correctly identified a spam email as spam).
* **True Negatives (TN):** The model correctly predicted the negative class. (e.g., correctly identified a non-spam email as not spam).
* **False Positives (FP):** The model incorrectly predicted the positive class. (e.g., a normal email was flagged as spam). Also known as a "Type I error."
* **False Negatives (FN):** The model incorrectly predicted the negative class. (e.g., a spam email was missed and went to the inbox). Also known as a "Type II error."

---
# Cost Function
A cost function (or loss function) is a mathematical function that measures the "cost" or "error" of a model's predictions compared to the actual true values. It quantifies how bad the model's performance is. The goal of training a machine learning model is to find the set of parameters (weights and biases) that minimizes this cost function.

For example, in a regression problem trying to predict house prices, a common cost function is the **Mean Squared Error (MSE)**. For each house, it calculates the difference between the predicted price and the actual price, squares this difference, and then averages these squared differences across all houses in the training set. A lower MSE means the model's predictions are closer to the real prices.

---
# Cross-Entropy
Cross-entropy is a widely used loss function for classification tasks. It measures the difference between two probability distributions: the predicted probability distribution from the model and the actual true distribution (where the correct class has a probability of 1 and all others have 0). A lower cross-entropy value means the model's predicted probabilities are closer to the true labels.

For example, if a model is trying to classify an image of a cat and it outputs probabilities `[cat: 0.9, dog: 0.05, bird: 0.05]`, the cross-entropy loss will be low because the predicted probability for the correct class is high. If it outputs `[cat: 0.2, dog: 0.7, bird: 0.1]`, the loss will be much higher.

***
## Formal Definition
For binary classification, the formula is Binary Cross-Entropy:

$$
L = -(y \log(p) + (1-y) \log(1-p))
$$

where:
* $y$ is the true label (0 or 1).
* $p$ is the predicted probability for the positive class.

---
# Data Augmentation
Data augmentation is a technique used to artificially increase the size and diversity of a training dataset by creating modified copies of existing data. For image data, this involves applying transformations like rotations, flips, zooms, and color shifts. This helps the model become more robust and prevents overfitting, as it learns to recognize objects in various conditions.

For example, if you are training a model to recognize cats, you can take one image of a cat and create dozens of new training examples by flipping it horizontally, rotating it slightly, cropping it differently, and adjusting its brightness.

---
# Data Imputation
Data imputation is the process of replacing missing values in a dataset with substituted values. Missing data is a common problem and can cause errors or produce biased models. Imputation techniques allow you to use models that would otherwise not work with missing data.

For example, if you have a dataset of customer information and some entries are missing the "Age" value, you could use a simple imputation method like replacing all missing ages with the mean (average) age of all the other customers. More complex methods might use a machine learning model to predict the missing age based on other customer features.

---
# Decision Tree
A decision tree is a supervised learning algorithm that is used for both classification and regression. It works by splitting the data into smaller and smaller subsets based on a series of questions about the input features, creating a tree-like model of decisions. Each internal node represents a "test" on a feature, each branch represents the outcome of the test, and each leaf node represents a class label or a continuous value.

For example, a decision tree could be used to decide whether to play tennis. It might first ask, "What is the weather outlook?" If `"Sunny"`, it might then ask, "What is the humidity?" If `"High"`, the decision might be `"Don't Play"`. If `"Normal"`, the decision might be `"Play"`.

---
# Deep Learning
Deep learning is a subfield of machine learning based on artificial neural networks with many layers (hence "deep"). These deep architectures allow the model to learn a hierarchy of features, from simple patterns in the early layers to complex, abstract concepts in the deeper layers. Deep learning is particularly powerful for tasks involving large amounts of unstructured data, like images, sound, and text.

For example, the AI that powers facial recognition on your phone uses a deep learning model. The first few layers might learn to detect edges and colors, the middle layers might learn to recognize shapes like eyes and noses, and the final layers learn to recognize the specific configuration of features that make up your face.

---
# Diffusion Model
A diffusion model is a type of generative model that learns to create new data by reversing a "diffusion" process. The process starts by taking a real image and progressively adding a small amount of Gaussian noise over many steps until it becomes pure noise. The model is then trained to learn how to reverse this process—starting from random noise, it learns to gradually remove the noise step-by-step to generate a clean, realistic image.

For example, modern text-to-image generators like DALL-E 3 and Midjourney are based on diffusion models. When you give them a prompt like "an astronaut riding a horse," the model starts with a field of random noise and, guided by the text, denoises it over many steps into a coherent image that matches the description.

---
# Dimensionality Reduction
Dimensionality reduction is the process of reducing the number of input variables (or features) in a dataset. High-dimensional data can be difficult to work with, leading to high computational costs and an increased risk of overfitting (the "curse of dimensionality"). Dimensionality reduction techniques transform the data into a lower-dimensional space while trying to preserve as much of the important information as possible.

For example, a dataset of customer information might have 100 different features. Dimensionality reduction could be used to combine these into 10 new "meta-features" that capture the most important variance in the data, making it much easier to train a model. **Principal Component Analysis (PCA)** is a popular technique for this.

---
# Dropout
Dropout is a regularization technique used in neural networks to prevent overfitting. During training, it randomly "drops out" (sets to zero) a certain proportion of neurons in a layer for each training step. This forces the network to learn more robust features and prevents it from becoming too reliant on any single neuron. It's like forcing a team to work together without knowing which members will be present on any given day, making each member more capable and less dependent on others.

For example, with a dropout rate of 0.5, each neuron has a 50% chance of being ignored during a single forward/backward pass. The "thinned" network has to learn to make accurate predictions even with a reduced set of neurons.

---
# DQN (Deep Q-Network)
A Deep Q-Network is a reinforcement learning algorithm that combines Q-learning with a deep neural network. In traditional Q-learning, the agent learns a table of "Q-values" that estimate the reward for taking an action in a given state. However, this is not feasible for complex environments with many states (like a video game screen). A DQN replaces this table with a deep neural network that takes the state (e.g., the pixels of the game screen) as input and outputs the Q-values for all possible actions.

For example, DeepMind used a DQN to learn to play classic Atari games. The agent was only given the raw pixel data from the screen and the game score as a reward signal. By using a DQN, it learned to play many games at a superhuman level.

---
# Embeddings
Embeddings are numerical representations of categorical or textual data in a low-dimensional continuous vector space. The key idea is that items with similar meanings or contexts are represented by vectors that are close to each other in this space. This allows machine learning models to work with concepts and relationships rather than just raw text or IDs.

For example, a word embedding model like **Word2Vec** would learn vector representations for words. The vectors for `"king"` and `"queen"` would be close to each other. Furthermore, the vector relationship `vector("king") - vector("man") + vector("woman")` would result in a vector that is very close to `vector("queen")`, capturing the gender and royalty analogy numerically.

---
# Ensemble Learning
Ensemble learning is a technique where multiple machine learning models (called "weak learners") are trained to solve the same problem, and their predictions are combined to produce a single, more accurate final prediction. The idea is that by combining the outputs of several models, you can reduce errors, improve robustness, and get better performance than any single model could achieve on its own. Common ensemble methods include **Bagging (e.g., Random Forest)** and **Boosting (e.g., Gradient Boosting)**.

For example, a **Random Forest** model builds hundreds of individual decision trees on different random subsets of the data and features. To make a final prediction, it takes a majority vote from all the trees, which is typically more accurate and less prone to overfitting than a single decision tree.

---
# Epoch
An epoch represents one complete pass of the entire training dataset through a machine learning algorithm. During one epoch, the model sees and learns from every single training example once. Training a model typically requires many epochs to allow the algorithm to iteratively adjust its parameters and minimize the cost function.

For example, if you have a dataset of 10,000 images and you set your training to run for 50 epochs, the model will process all 10,000 images a total of 50 times.

---
# Exploding Gradient
The exploding gradient problem is an issue that can occur during the training of deep neural networks, where the gradients (error signals) become excessively large during backpropagation. This causes the model's weights to be updated by huge amounts, leading to unstable training where the loss oscillates wildly or diverges to infinity. It's the opposite of the vanishing gradient problem.

For example, this can happen in Recurrent Neural Networks (RNNs) when processing long sequences. A large gradient can be compounded as it's propagated back through many time steps, causing the weights to "explode." A common technique to mitigate this is **gradient clipping**, which caps the gradients at a certain threshold.

---
# F1-Score
The F1-Score is a metric used to evaluate the performance of a classification model. It is the harmonic mean of **Precision** and **Recall**, and it provides a single score that balances both metrics. It is particularly useful when you have an uneven class distribution (e.g., many more negative examples than positive ones).

For example, in a medical diagnosis task to detect a rare disease, you want both high precision (to avoid telling healthy people they are sick) and high recall (to avoid missing people who actually have the disease). The F1-Score combines these two needs into one number.

***
## Formal Definition

$$
F_1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$

---
# Feature Engineering
Feature engineering is the process of using domain knowledge to create new input variables (features) from raw data to improve the performance of a machine learning model. A well-engineered feature can make a complex problem much simpler for the model to learn. This can involve combining existing features, decomposing them, or creating entirely new ones.

For example, if you have raw timestamp data, you could engineer new features like:
* `day_of_week` (Monday, Tuesday, etc.)
* `month` (January, February, etc.)
* `is_weekend` (True/False)
These new features might be much more predictive for a sales forecasting model than the raw timestamp alone.

---
# GAN (Generative Adversarial Network)
A Generative Adversarial Network is a type of generative model that consists of two competing neural networks: a **Generator** and a **Discriminator**.
* The **Generator's** job is to create fake, synthetic data (e.g., images) that looks realistic.
* The **Discriminator's** job is to act as a detective and distinguish between real data and the fake data created by the generator.
The two networks are trained together in a zero-sum game. The generator gets better at creating convincing fakes, while the discriminator gets better at spotting them. This adversarial process pushes the generator to produce incredibly realistic data.

For example, GANs can be used to generate photorealistic images of human faces of people who do not exist.

---
# GLoVe (Global Vectors for Word Representation)
GLoVe is an unsupervised learning algorithm for obtaining vector representations (embeddings) for words. It works by training on aggregated global word-word co-occurrence statistics from a large corpus. The main idea is that the ratio of co-occurrence probabilities of two words with a third "probe" word can encode meaning. GLoVe learns word vectors such that their dot product equals the logarithm of their co-occurrence probability.

For example, GLoVe would learn that the co-occurrence ratio of `ice` and `steam` with the probe word `solid` is high, while with the probe word `gas` it is low, and it would encode this relationship in the learned vectors.

---
# GNN (Graph Neural Network)
A Graph Neural Network is a type of neural network designed specifically to work with data structured as a graph (nodes connected by edges). GNNs work by passing messages between nodes. Each node aggregates information from its neighbors to update its own state or representation. This process is repeated across multiple layers, allowing the GNN to capture complex relationships and structural information within the graph.

For example, in a social network, a GNN could be used to predict user interests. It would learn a representation for each user (node) by aggregating information from their friends (neighbors), allowing it to make recommendations based on the community structure.

---
# GPT (Generative Pre-trained Transformer)
GPT is a family of large language models developed by OpenAI that are based on the **Transformer** architecture. The "Generative Pre-trained" part of the name describes its two-stage training process:
1.  **Pre-training:** The model is trained on a massive amount of unlabeled text data from the internet in a self-supervised way. Its task is simple: predict the next word in a sequence. By doing this billions of times, it learns grammar, facts, reasoning abilities, and a representation of the world.
2.  **Fine-tuning:** The pre-trained model is then adapted for specific downstream tasks (like question answering or summarization) by training it on a much smaller, labeled dataset.

For example, ChatGPT is a version of a GPT model that has been fine-tuned through a process called RLHF to be a helpful conversational assistant.

---
# Gradient Boosting
Gradient Boosting is a powerful ensemble learning technique that builds a predictive model in the form of an ensemble of weak prediction models, typically decision trees. It builds the model in a stage-wise fashion. In each stage, it identifies the shortcomings of the existing model by looking at the errors (residuals) and fits a new weak learner to these errors. It "boosts" the performance by sequentially adding new models that correct the mistakes of the previous ones.

For example, in predicting a house price, the first tree might make a rough prediction. The second tree will then be trained not on the house features, but on the *error* of the first tree's prediction. By adding the prediction of this second tree to the first, the overall prediction gets closer to the true value. This process is repeated many times.

---
# Gradient Descent
Gradient descent is an iterative optimization algorithm used to find the minimum value of a function, typically the cost function in machine learning. It works by taking steps in the direction of the negative gradient (the direction of steepest descent) of the function at the current point. The size of these steps is determined by the **learning rate**.

Imagine you are standing on a foggy mountain and want to get to the lowest point. You can't see the bottom, but you can feel the slope of the ground beneath your feet. Gradient descent is like taking a small step in the steepest downhill direction, then re-evaluating the slope and taking another step, repeating until you reach the bottom (the minimum of the cost function).

---
# GRU (Gated Recurrent Unit)
A Gated Recurrent Unit is a type of Recurrent Neural Network (RNN) that uses a gating mechanism to control the flow of information. It is a simplified version of the LSTM unit, with fewer parameters. It has two main gates:
* **Update Gate:** Decides how much of the past information (from previous time steps) to keep and how much new information to add.
* **Reset Gate:** Decides how much of the past information to forget.
By using these gates, GRUs can capture long-term dependencies in sequential data while mitigating the vanishing gradient problem.

---
# Hyperparameter Tuning
Hyperparameter tuning is the process of finding the optimal set of hyperparameters for a machine learning model to achieve the best performance. Hyperparameters are configuration settings that are not learned from the data but are set before the training process begins (e.g., learning rate, number of layers). This process often involves systematically testing different combinations of values.

For example, you might use **Grid Search**, where you define a grid of possible values for your hyperparameters (e.g., learning rates of `0.1, 0.01, 0.001` and batch sizes of `32, 64`). The tuning process will then train and evaluate the model for every single combination on the grid to find the one that performs best.

---
# Hyperparameters
Hyperparameters are external configuration variables for a machine learning model that cannot be learned from the data. They are set by the data scientist before the training process starts and they control how the model is structured and how it learns. The choice of hyperparameters can have a significant impact on the model's performance.

Examples of common hyperparameters include:
* The **learning rate** in gradient descent.
* The **number of epochs** (how many times to cycle through the training data).
* The **number of layers** in a neural network.
* The **number of trees** in a random forest.

---
# Inception Network
The Inception Network (or GoogLeNet) is a deep convolutional neural network architecture that introduced the "Inception module." The key idea of this module is to perform multiple different-sized convolutions (e.g., 1x1, 3x3, 5x5) and a max-pooling operation in parallel within the same layer. The outputs of these parallel branches are then concatenated together. This allows the network to capture features at multiple scales simultaneously and improves computational efficiency by using 1x1 convolutions for dimensionality reduction.

---
# Instance Segmentation
Instance segmentation is a computer vision task that is more advanced than both object detection and semantic segmentation. It not only classifies each pixel in an image but also distinguishes between different instances of the same object class.

For example, in an image with three cars, semantic segmentation would label all car pixels as "car." Object detection would draw three separate bounding boxes, one for each car. Instance segmentation would go a step further and produce three distinct pixel masks, one for each individual car, perfectly outlining each one separately.

---
# K-Fold Cross Validation
K-Fold Cross-Validation is a technique used to evaluate the performance of a machine learning model and ensure it generalizes well to new data. The process involves splitting the entire dataset into *k* equal-sized "folds." Then, the model is trained and evaluated *k* times. In each iteration, one fold is used as the testing set, and the remaining *k-1* folds are used as the training set. The final performance metric is the average of the results from the *k* iterations.

For example, in 5-fold cross-validation, the data is split into 5 folds. The model is trained on folds 1-4 and tested on fold 5. Then trained on folds 1,2,3,5 and tested on fold 4, and so on. This gives a more robust estimate of the model's performance than a single train-test split.

---
# K-Means Clustering
K-Means is a popular unsupervised learning algorithm used for clustering. It aims to partition a dataset into *k* distinct, non-overlapping clusters. It works iteratively:
1.  **Initialization:** Randomly select *k* data points to be the initial cluster centers (centroids).
2.  **Assignment:** Assign each data point to the nearest centroid.
3.  **Update:** Recalculate the centroid of each cluster by taking the mean of all data points assigned to it.
4.  **Repeat:** Repeat steps 2 and 3 until the cluster assignments no longer change.

---
# K-Nearest Neighbors (KNN)
K-Nearest Neighbors is a simple, non-parametric supervised learning algorithm used for both classification and regression. To make a prediction for a new data point, it looks at the *k* closest data points (its "nearest neighbors") in the training set.
* For **classification**, it assigns the class that is most common among its *k* neighbors (a majority vote).
* For **regression**, it assigns the average of the values of its *k* neighbors.

For example, to classify a new fruit, KNN with k=5 would find the 5 fruits in the training data that are most similar to it based on features like color, size, and shape. If 3 of those 5 neighbors are apples, it will classify the new fruit as an apple.

---
# Large Language Model (LLM)
A Large Language Model is an advanced AI model, typically based on the Transformer architecture, that has been trained on vast quantities of text data. LLMs are characterized by their massive size (billions of parameters) and their emergent ability to understand, generate, summarize, translate, and interact with human language in a coherent and contextually relevant way.

Examples of prominent LLMs include OpenAI's GPT series (e.g., GPT-4), Google's Gemini, and Meta's LLaMA. They power applications like chatbots, content creation tools, and sophisticated search engines.

---
# Learning Rate
The learning rate is a crucial hyperparameter in optimization algorithms like gradient descent. It controls the size of the steps the algorithm takes to move toward the minimum of the cost function.
* A **small learning rate** will result in slow but reliable training, as it takes tiny steps. However, it might get stuck in a local minimum.
* A **large learning rate** allows the model to learn faster, but it risks overshooting the minimum and failing to converge, causing the loss to oscillate or diverge.
Choosing an appropriate learning rate is critical for successful model training.

---
# Lemmatization
Lemmatization is a text normalization technique in NLP that reduces a word to its base or dictionary form, known as the **lemma**. Unlike stemming, which simply chops off prefixes and suffixes, lemmatization uses a dictionary and morphological analysis to determine the proper root word. This makes it more accurate but also more computationally expensive than stemming.

For example:
* The word `"better"` would be correctly lemmatized to its lemma, `"good"`.
* The words `"running"`, `"ran"`, and `"runs"` would all be lemmatized to `"run"`.

---
# Linear Regression
Linear regression is a supervised learning algorithm that models the relationship between a dependent variable and one or more independent variables by fitting a linear equation (a straight line) to the observed data. The goal is to find the line that minimizes the distance between the line and the actual data points.

For example, a company could use linear regression to model the relationship between its advertising spending (independent variable) and its monthly sales (dependent variable). The resulting model could then be used to predict future sales based on a planned advertising budget.

---
# Logistic Regression
Logistic regression is a supervised learning algorithm used for binary classification tasks (where the outcome is one of two classes). Despite its name, it is a classification algorithm, not a regression one. It works by using a logistic (or sigmoid) function to model the probability of a certain class or event existing, such as pass/fail, win/lose, or spam/not spam. The output is a probability between 0 and 1, which can be converted to a class prediction by setting a threshold (usually 0.5).

For example, a bank could use logistic regression to predict whether a loan applicant will default or not. Based on features like income, credit score, and age, the model would output the probability of default.

---
# Loss Function
A loss function (or cost function) is a method of evaluating how well a specific algorithm models the given data. If the model's predictions are far from the true values, the loss function will output a large number. If they are close, it will output a smaller number. The process of training a model involves trying to find the set of weights and biases that minimize the value of the loss function.

For example, **Mean Squared Error (MSE)** is a common loss function for regression tasks. It is calculated as the average of the squared differences between the predicted and actual values.

---
# LSTM (Long Short-Term Memory)
An LSTM is a special type of Recurrent Neural Network (RNN) architecture that is specifically designed to learn long-term dependencies in sequential data. It solves the vanishing gradient problem that standard RNNs face. LSTMs have a more complex cell structure that includes three "gates":
* **Forget Gate:** Decides what information to throw away from the cell state.
* **Input Gate:** Decides which new information to store in the cell state.
* **Output Gate:** Decides what to output based on the cell state.
This gating mechanism allows the network to remember information for long periods.

---
# Machine Learning
Machine learning is a branch of artificial intelligence that gives computers the ability to learn from data without being explicitly programmed. Instead of having hard-coded rules, a machine learning model learns patterns and relationships directly from a training dataset. The model's performance on a task improves as it is exposed to more data.

Machine learning is divided into three main subtypes:
1.  **Supervised Learning:** Learning from labeled data (e.g., classification, regression).
2.  **Unsupervised Learning:** Finding patterns in unlabeled data (e.g., clustering).
3.  **Reinforcement Learning:** Learning through trial and error with rewards and punishments.

---
# Markov Decision Process (MDP)
A Markov Decision Process is a mathematical framework for modeling decision-making in situations where outcomes are partly random and partly under the control of a decision-maker. It is the fundamental framework for reinforcement learning. An MDP is defined by a set of states, a set of actions, a transition function that gives the probability of moving from one state to another given an action, and a reward function. The goal is to find a "policy" (a strategy for choosing actions in states) that maximizes the cumulative reward over time.

---
# Naive Bayes
Naive Bayes is a simple but effective probabilistic classification algorithm based on **Bayes' Theorem**. It is "naive" because it makes a strong assumption that all the input features are independent of one another, which is often not true in the real world. Despite this simplistic assumption, Naive Bayes classifiers work very well in practice, especially for text classification tasks like spam filtering.

***
## Formal Definition
Based on Bayes' Theorem:

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$
In the context of classification, this is expressed as:
$$
P(\text{class}|\text{features}) = \frac{P(\text{features}|\text{class}) \cdot P(\text{class})}{P(\text{features})}
$$

---
# NER (Named Entity Recognition)
Named Entity Recognition is an NLP task focused on locating and classifying named entities in unstructured text into predefined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, etc.

For example, in the text "Apple, founded by Steve Jobs in Cupertino, is planning a new product launch in September," an NER system would identify:
* `"Apple"` as an **Organization**.
* `"Steve Jobs"` as a **Person**.
* `"Cupertino"` as a **Location**.
* `"September"` as a **Date**.

---
# NLP (Natural Language Processing)
Natural Language Processing is a field of AI that gives computers the ability to understand, interpret, and generate human language. It involves tasks that allow machines to process and analyze large amounts of natural language data, from text to speech.

Key NLP tasks include:
* **Text Classification:** Assigning categories to text (e.g., sentiment analysis).
* **Information Extraction:** Pulling specific pieces of information from text (e.g., NER).
* **Machine Translation:** Translating text from one language to another.
* **Text Generation:** Creating new, human-like text.

---
# Normalization
Normalization is a data preprocessing technique used to scale the values of features in a dataset to a common, standard range. This is important because features with very different scales can cause machine learning algorithms (especially those that use distance calculations, like KNN, or rely on gradient descent) to perform poorly. A common normalization technique is **Min-Max Scaling**, which scales all data to a fixed range, usually 0 to 1.

For example, if you have a dataset with `age` (ranging from 20-70) and `income` (ranging from 30,000-200,000), the income feature would dominate any distance calculation. Normalization would scale both features to the 0-1 range, giving them equal weight.

---
# Optimizer
An optimizer is an algorithm used during the training of a neural network that modifies the model's parameters (weights and biases) to minimize the cost function. It implements the gradient descent algorithm or one of its variants. The optimizer uses the gradients calculated by backpropagation to determine the direction and magnitude of the weight updates.

Common optimizers include:
* **SGD (Stochastic Gradient Descent):** A basic optimizer.
* **Adam (Adaptive Moment Estimation):** A more advanced and widely used optimizer that adapts the learning rate for each parameter, often leading to faster convergence.

---
# Overfitting
Overfitting is a common error in machine learning where a model learns the training data *too well*. It memorizes the noise and specific details in the training set to the point where it fails to generalize to new, unseen data. An overfitted model will have very high accuracy on the training data but will perform poorly on the testing data.

For example, imagine a student who memorizes the exact answers to every question in a practice exam but doesn't understand the underlying concepts. They will ace the practice exam, but when given a real exam with slightly different questions, they will fail. This is overfitting. Techniques like **regularization** and **dropout** are used to prevent it.

---
# Parameters
Parameters are the internal variables of a machine learning model that are learned directly from the training data. They are the values that the model uses to make predictions. The process of "training" or "learning" is essentially the process of finding the optimal values for these parameters.

For example:
* In a **linear regression** model ($y = \beta_0 + \beta_1x$), the parameters are the intercept ($\beta_0$) and the slope ($\beta_1$).
* In a **neural network**, the parameters are all the **weights** and **biases** of the connections between neurons.

---
# PCA (Principal Component Analysis)
PCA is a popular unsupervised learning technique used for dimensionality reduction. It works by transforming a set of possibly correlated variables into a new set of uncorrelated variables called **principal components**. These new components are ordered so that the first few retain most of the variation present in all of the original variables. By keeping only the first few principal components, you can reduce the dimensionality of the data while losing minimal information.

For example, PCA can be used for image compression. It can find the principal components of the pixel data, and by storing only the most significant components, it can reconstruct the image with high fidelity using much less data.

---
# Perceptron
The perceptron is the simplest form of an artificial neural network, consisting of a single neuron. It takes several binary inputs, applies a weight to each input, sums them up, and if the sum exceeds a certain threshold, it outputs a 1; otherwise, it outputs a 0. It is a linear binary classifier and can be seen as the fundamental building block of more complex neural networks.

---
# POS (Part-of-Speech) Tagging
Part-of-Speech Tagging is the process in NLP of marking up a word in a text as corresponding to a particular part of speech (like noun, verb, adjective, adverb, etc.). This is done based on both its definition and its context in the sentence. POS tagging is a crucial step for many downstream NLP tasks, as it provides syntactic information.

For example, in the sentence "The old man can still can the vegetables," a POS tagger would identify:
* The first `"can"` as a **modal verb**.
* The second `"can"` as a **verb**.

---
# Precision
Precision is a performance metric for a classification model that answers the question: "Of all the predictions I made for the positive class, how many were actually correct?" It is the ratio of true positives to the total number of positive predictions made by the model. High precision means that the model has a low false positive rate.

For example, in a spam filter, high precision is very important. You want to be sure that when an email is flagged as spam, it really is spam. You would rather a few spam emails get through (low recall) than have important emails incorrectly marked as spam (low precision).

***
## Formal Definition

$$
\text{Precision} = \frac{\text{True Positives (TP)}}{\text{True Positives (TP)} + \text{False Positives (FP)}}
$$

---
# Q-Learning
Q-Learning is a model-free reinforcement learning algorithm that learns a policy telling an agent what action to take under what circumstances. It works by learning a **Q-value function** that estimates the "quality" or expected future reward of taking a certain action in a certain state. The agent explores the environment and updates its Q-values based on the rewards it receives, gradually learning the optimal actions to take to maximize its cumulative reward.

For example, a robot learning to navigate a maze could use Q-learning. Each position in the maze is a state, and actions are move-up, down, left, right. The robot gets a positive reward for reaching the exit and a negative reward for hitting a wall. Through trial and error, it updates its Q-table to learn the best path.

---
# RAG (Retrieval-Augmented Generation)
RAG is an architecture that enhances the capabilities of large language models (LLMs) by connecting them to external knowledge sources. When a query is given to a RAG system, it first **retrieves** relevant documents or information from a database (often a vector database). It then **augments** the original prompt with this retrieved information and feeds the combined text to the LLM to **generate** a more accurate, up-to-date, and contextually aware response. This helps reduce hallucinations and allows the LLM to use proprietary or real-time data.

---
# Random Forest
A Random Forest is a powerful ensemble learning algorithm used for classification and regression. It operates by constructing a multitude of decision trees during training. For each tree, it uses a random subset of the training data (bagging) and a random subset of the features for splitting nodes. To make a prediction, it aggregates the results from all the individual trees—by taking a majority vote for classification or the average for regression. This process corrects for the tendency of single decision trees to overfit.

---
# Recall
Recall is a performance metric for a classification model that answers the question: "Of all the actual positive instances, how many did my model correctly identify?" It is the ratio of true positives to the total number of actual positive instances. High recall means that the model has a low false negative rate. It is also known as **sensitivity** or the **true positive rate**.

For example, in a medical test for a serious disease, high recall is critical. You want to correctly identify everyone who actually has the disease. It is better to have some false positives (low precision) than to miss a case (low recall).

***
## Formal Definition

$$
\text{Recall} = \frac{\text{True Positives (TP)}}{\text{True Positives (TP)} + \text{False Negatives (FN)}}
$$

---
# Regression
Regression is a supervised learning task where the goal is to predict a continuous numerical value. Unlike classification, which predicts a category, regression models predict a quantity. The model learns the relationship between the input features and the continuous output variable from the training data.

For example, predicting the price of a house, the temperature tomorrow, or the stock price of a company are all regression tasks.

---
# Regularization
Regularization is a set of techniques used to prevent overfitting in machine learning models. It works by adding a penalty term to the cost function that discourages the model from becoming too complex. This penalty term is based on the size of the model's parameters (weights). By penalizing large weights, regularization encourages the model to find a simpler solution that generalizes better to new data.

Common regularization techniques include:
* **L1 Regularization (Lasso):** Adds a penalty equal to the absolute value of the magnitude of coefficients. It can shrink some coefficients to exactly zero, effectively performing feature selection.
* **L2 Regularization (Ridge):** Adds a penalty equal to the square of the magnitude of coefficients. It shrinks coefficients but doesn't set them to zero.

---
# Reinforcement Learning
Reinforcement Learning is a type of machine learning where an **agent** learns to make decisions by performing actions in an **environment** to maximize a cumulative **reward**. The agent learns through trial and error. It receives positive rewards for desirable actions and negative rewards (or punishments) for undesirable ones. The goal of the agent is to learn a **policy**, which is a strategy for choosing actions that will maximize its total reward over time.

For example, training a dog is a form of reinforcement learning. The dog is the agent, the house is the environment. When it performs a good action (like sitting on command), it gets a reward (a treat). When it performs a bad action (like chewing the furniture), it gets a punishment (a scolding). Over time, it learns the policy that maximizes treats.

---
# ReLU (Rectified Linear Unit) Function
ReLU is an activation function widely used in deep neural networks. It is defined very simply: it outputs the input directly if the input is positive, and it outputs zero if the input is negative or zero. Despite its simplicity, it is highly effective and has become the default activation function for many types of neural networks. It helps to mitigate the vanishing gradient problem and is computationally very efficient.

***
## Formal Definition

$$
f(x) = \max(0, x)
$$

---
# ResNet (Residual Network)
A ResNet is a deep neural network architecture that introduced the concept of **residual connections** or **skip connections**. These connections allow the gradient to be directly backpropagated to earlier layers by creating a "shortcut" that skips over one or more layers. This technique effectively combats the vanishing gradient problem, which made it very difficult to train extremely deep neural networks. By using these residual blocks, ResNets can be built with hundreds or even thousands of layers while still being trainable.

---
# RLHF (Reinforcement Learning from Human Feedback)
RLHF is a technique used to fine-tune language models to better align with human preferences and values. The process involves three steps:
1.  A pre-trained LLM generates several responses to a prompt.
2.  Human evaluators rank these responses from best to worst.
3.  This ranking data is used to train a **reward model**. This reward model learns to predict which responses humans would prefer.
4.  Finally, the original LLM is fine-tuned using reinforcement learning, with the reward model providing the reward signal. The LLM learns a policy to generate responses that maximize the score from the reward model, effectively making it more helpful and aligned with human expectations.

---
# RNN (Recurrent Neural Network)
An RNN is a type of neural network designed to work with sequential data, such as time series or text. Unlike standard feedforward networks, RNNs have loops in them, allowing them to maintain a "memory" or **hidden state** that captures information about what has been processed so far. The output for the current time step is influenced by the previous computations.

For example, when processing the sentence "The clouds are in the ___", an RNN would use the memory of the words "clouds" and "are" to predict that the next word is likely to be "sky".

---
# ROC Curve (Receiver Operating Characteristic Curve)
An ROC curve is a graph used to evaluate the performance of a binary classification model at all classification thresholds. It plots the **True Positive Rate (Recall)** against the **False Positive Rate** at various threshold settings.
* A model with no predictive power would have an ROC curve that is a diagonal line.
* A perfect model would have a curve that goes straight up the y-axis and then across the x-axis.
The **Area Under the Curve (AUC)** is a single metric that summarizes the ROC curve. An AUC of 1.0 represents a perfect model, while an AUC of 0.5 represents a worthless model.

---
# Self-Supervised Learning
Self-supervised learning is a type of machine learning where a model learns from data without human-provided labels. Instead, the labels are generated automatically from the input data itself. The model is given a pretext task where it has to predict a hidden part of its input from the visible part. By solving this task on a massive amount of unlabeled data, the model learns a rich, useful representation of the data that can then be fine-tuned for downstream supervised tasks.

For example, a language model like BERT uses a self-supervised task called **Masked Language Modeling**. It takes a sentence, randomly masks some of the words, and its goal is to predict the original masked words.

---
# Semantic Segmentation
Semantic segmentation is a computer vision task that involves classifying every pixel in an image with a corresponding class label. It creates a dense, pixel-level map of the image, identifying the category of each pixel (e.g., "road," "car," "pedestrian," "sky"). It does not, however, distinguish between different instances of the same class.

For example, in a street scene, it would color all pixels belonging to any car with the same color, say red, without differentiating between the individual cars.

---
# Sigmoid Function
The sigmoid function is a mathematical function that produces an "S"-shaped curve. It takes any real-valued number as input and maps it to a value between 0 and 1. Because its output can be interpreted as a probability, it is commonly used as the activation function in the output layer of a neural network for binary classification problems.

***
## Formal Definition

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

---
# Softmax
The softmax function is an activation function that converts a vector of raw scores (logits) into a probability distribution. It takes a vector of real numbers and transforms them into probabilities that sum to 1. It does this by exponentiating each score (making them all positive) and then dividing each by the sum of all the exponentiated scores. It is used as the activation function for the output layer in multi-class classification problems.

For example, in a model classifying an image as a cat, dog, or bird, the final layer might output raw scores of `[3.0, 1.0, 0.2]`. The softmax function would convert these into a probability distribution like `[0.836, 0.113, 0.051]`, clearly identifying "cat" as the most likely class with 83.6% probability.
 
***
## Formal Definition

Given an input vector $z$ of $K$ real numbers, where $z = (z_1, z_2, \dots, z_K)$, the softmax function $\sigma(z)_i$ for the $i$-th element is defined as:

$$
\begin{align*}
\sigma(z)_i &= \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}} \\
\\
\text{where:} \\
z_i &= \text{ the } i\text{-th element of the input vector} \\
e^{z_i} &= \text{ the standard exponential function applied to } z_i \\
K &= \text{ the number of elements in the vector (or classes)} \\
\sum_{j=1}^{K} e^{z_j} &= \text{ the normalization term, ensuring all outputs sum to 1}
\end{align*}
$$

---
# Specificity
Specificity is a performance metric for a classification model that measures the proportion of actual negatives that are correctly identified as such. It answers the question: "Of all the instances that were actually negative, how many did my model correctly identify?" It is also known as the **true negative rate**. High specificity means the model has a low false positive rate.

For example, in a legal setting to determine guilt, high specificity is crucial. You want to correctly identify all innocent people as innocent. A low specificity would mean many innocent people are incorrectly flagged as guilty.

***
## Formal Definition

$$
\text{Specificity} = \frac{\text{True Negatives (TN)}}{\text{True Negatives (TN)} + \text{False Positives (FP)}}
$$

---
# Stemming
Stemming is a text normalization technique in NLP that reduces words to their root or "stem" form by algorithmically chopping off prefixes and suffixes. It is a crude, rule-based process that is fast but can sometimes result in stems that are not actual words.

For example:
* The words `"computer"`, `"computing"`, `"computes"` might all be stemmed to `"comput"`.
* The words `"argue"`, `"argued"`, `"argues"` might be stemmed to `"argu"`.

---
# Stop Words
Stop words are commonly used words in a language (like "a", "the", "is", "in", "on") that are often filtered out during the preprocessing of text data in NLP. These words are considered to be "noise" because they occur very frequently but typically do not carry significant semantic meaning that would help a model distinguish between documents. Removing them helps reduce the dimensionality of the data and allows the model to focus on more important keywords.

---
# Supervised Learning
Supervised learning is a type of machine learning where the model is trained on a dataset that is **labeled**. This means that for every input example in the training data, there is a corresponding correct output label. The model learns by comparing its own output with the correct labels and adjusting its parameters to reduce the error. The two main types of supervised learning tasks are **classification** (predicting a category) and **regression** (predicting a continuous value).

For example, training a model to identify cats in images is a supervised learning task. You would need a large dataset of images, where each image is labeled as either "cat" or "not cat."

---
# SVM (Support Vector Machine)
A Support Vector Machine is a powerful supervised learning algorithm used for classification and regression. In its most common form, it works by finding the optimal hyperplane (a boundary line) that best separates the data points of different classes in a high-dimensional space. The "optimal" hyperplane is the one that has the largest margin—the maximum distance—between itself and the nearest data points of any class. These nearest points are called the **support vectors**.

For example, in a 2D space, an SVM would find the straight line that best separates two classes of points while being as far away from the points on either side as possible.

---
# TF-IDF (Term Frequency-Inverse Document Frequency)
TF-IDF is a statistical measure used to evaluate the importance of a word in a document relative to a collection of documents (a corpus). It is a common technique for vectorizing text. It combines two metrics:
* **Term Frequency (TF):** How often a word appears in a specific document.
* **Inverse Document Frequency (IDF):** A measure of how rare a word is across all documents in the corpus. Words that appear everywhere (like "the") have a low IDF score.
The TF-IDF score is high for words that appear frequently in one document but rarely in others, making them good indicators of the document's topic.

***
## Formal Definition

$$
\text{TF-IDF}(t, d, D) = \text{TF}(t, d) \cdot \text{IDF}(t, D)
$$

where $\text{IDF}(t, D) = \log\left(\frac{N}{|\{d \in D: t \in d\}|}\right)$
* $t$ is the term, $d$ is the document, $D$ is the corpus.
* $N$ is the total number of documents in the corpus.

---
# Tokenization
Tokenization is the first step in any NLP pipeline. It is the process of breaking down a piece of text into smaller units called **tokens**. These tokens can be words, characters, or sub-words. This process is essential because machine learning models need to process text as a sequence of discrete items rather than a single long string.

For example, the sentence `"AI is transforming the world."` can be tokenized into the following list of word tokens:
`["AI", "is", "transforming", "the", "world", "."]`

---
# Transfer Learning
Transfer learning is a machine learning technique where a model developed for a specific task is reused as the starting point for a model on a second, related task. Instead of training a new model from scratch, you leverage the knowledge (features, weights) that a pre-trained model has already learned from a large dataset. This is particularly useful when you have a limited amount of data for your specific task.

For example, a model pre-trained on the massive ImageNet dataset (which has millions of images of thousands of object types) has already learned to recognize general visual features like edges, textures, and shapes. You can take this pre-trained model and fine-tune it on your small, specific dataset of medical X-ray images to classify diseases. This will be much faster and more effective than training a model from scratch on only the X-rays.

---
# Transformer
The Transformer is a revolutionary neural network architecture that relies entirely on the **self-attention mechanism** to process sequential data. It was introduced in the paper "Attention Is All You Need." Unlike RNNs and LSTMs, it does not process data in order. Instead, it can process all tokens in a sequence simultaneously and uses self-attention to weigh the importance of all other tokens in the sequence when encoding a representation for a given token. This parallel processing capability and its effectiveness at capturing long-range dependencies have made it the foundation for most modern large language models, like GPT and BERT.

---
# U-Net
U-Net is a convolutional neural network architecture designed specifically for biomedical image segmentation. It is famous for its characteristic "U"-shaped architecture, which consists of two paths:
1.  A **contracting path (encoder)** that follows the typical CNN architecture to capture context. It uses convolutional and max-pooling layers to downsample the image.
2.  A **symmetric expanding path (decoder)** that uses transposed convolutions to upsample the feature maps, enabling precise localization.
Crucially, it uses **skip connections** to concatenate the feature maps from the encoder path with the corresponding upsampled feature maps from the decoder path. This allows the network to combine high-level contextual information with fine-grained spatial information to produce very precise segmentation maps.

---
# Underfitting
Underfitting is a modeling error that occurs when a machine learning model is too simple to capture the underlying structure of the data. It fails to learn the relationship between the input and output variables. An underfitted model will have poor performance on both the training data and the testing data. It is a sign of **high bias**.

For example, trying to fit a straight line to data that has a clear non-linear, parabolic shape would result in underfitting. The model is not complex enough to capture the true pattern.

---
# Unsupervised Learning
Unsupervised learning is a type of machine learning where the model is trained on **unlabeled** data. The algorithm tries to learn the patterns, structures, and relationships directly from the data without any corresponding output labels. The goal is to discover the inherent structure of the data.

The most common unsupervised learning tasks are:
* **Clustering:** Grouping similar data points together.
* **Dimensionality Reduction:** Reducing the number of variables in the data.
* **Association Rule Mining:** Discovering relationships between variables in large datasets.

---
# Vanishing Gradient
The vanishing gradient problem is an issue that occurs during the training of deep neural networks, particularly RNNs. During backpropagation, the gradients of the loss function can become exponentially smaller as they are propagated backward through the layers. As a result, the weights of the early layers of the network are updated very slowly, or not at all, which means they fail to learn. This makes it very difficult to train deep networks. Architectures like LSTMs and ResNets were specifically designed to combat this problem.

---
# Variance
In machine learning, variance is a type of error that occurs when a model is too complex and learns the random noise in the training data instead of the underlying signal. A high-variance model is overly sensitive to small fluctuations in the training set. This results in **overfitting**, where the model performs very well on the training data but fails to generalize to new, unseen data.

For example, fitting a very complex, high-degree polynomial curve to a set of data points that have a simple linear relationship would be a high-variance model. It would wiggle and bend to pass through every single training point perfectly but would make poor predictions for any new points.

---
# Word2Vec
Word2Vec is a popular technique to learn word embeddings (vector representations of words). It is a shallow, two-layer neural network that is trained to reconstruct the linguistic contexts of words. It takes a large corpus of text as its input and produces a vector space, typically of several hundred dimensions, with each unique word in the corpus being assigned a corresponding vector in the space. Words that share common contexts in the corpus are located close to one another in the vector space.

For example, it would learn that words like "dog," "puppy," and "canine" are used in similar contexts and would therefore have similar vectors.

---
# XGBoost (Extreme Gradient Boosting)
XGBoost is an optimized and highly efficient implementation of the **gradient boosting** algorithm. It is known for its high performance and speed. It improves upon the standard gradient boosting framework by incorporating several advanced features, including:
* **Regularization (L1 and L2):** To prevent overfitting.
* **Parallel Processing:** For faster training.
* **Handling Missing Values:** It has a built-in routine to handle missing data.
* **Tree Pruning:** It grows the tree up to a max depth and then prunes it backward.
XGBoost is often the winning algorithm in many machine learning competitions on tabular data.

---
# YOLO (You Only Look Once)
YOLO is a state-of-the-art, real-time object detection system. Its key innovation is that it frames object detection as a single regression problem, directly predicting bounding box coordinates and class probabilities from the full image in one pass. Unlike other models that apply a classifier to many different regions of an image, YOLO looks at the entire image just once, making it extremely fast and suitable for real-time applications like video analysis.

---
# Zero-Shot Learning
Zero-shot learning is a machine learning paradigm where a model can classify data from classes it has never seen during training. It works by leveraging a high-level description of the classes (e.g., a set of attributes or a text description) and learning a mapping between the visual feature space and this semantic space.

For example, a model could be trained to recognize horses, pandas, and tigers by learning their visual features and their semantic attributes (e.g., a tiger "has stripes," "is a carnivore"). To recognize a "zebra" (a class it has never seen), it could be told that a zebra "has stripes" and "is a herbivore." By combining the learned visual concept of "stripes" with the new semantic information, it can successfully identify a zebra without ever having been trained on a zebra image.
