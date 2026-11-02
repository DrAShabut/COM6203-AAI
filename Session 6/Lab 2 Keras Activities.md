
# Laboratory Activities: Image and Video Classification Using CNNs

These laboratory activities build on the practical work with Artificial Neural Networks and Convolutional Neural Networks (CNNs). You will use two Keras examples to explore how CNNs can classify images and videos, experiment with model configurations, and evaluate model performance.

---

# Activity 1: Image Classification Using a CNN

**Reference:** [Image Classification from Scratch – Keras](https://keras.io/examples/vision/image_classification_from_scratch/)

## Aim

To build and experiment with a CNN that classifies images into categories.

## Learning Outcomes

By the end of this activity, you should be able to:

- Explain the main stages of an image classification pipeline.
- Prepare image datasets for training and validation.
- Identify the role of convolutional and pooling layers.
- Train and evaluate a CNN.
- Investigate how model configuration affects classification performance.

## Task 1: Explore the Example

1. Open the Keras example.
2. Read through the notebook and identify the main stages of the implementation.
3. Run the example and observe the output.

**Questions**

1. What dataset is used in the example?
2. What are the input and output of the CNN?
3. What is the purpose of the convolutional layers?
4. Why is the dataset divided into training and validation sets?
5. What is the purpose of image augmentation?

## Task 2: Experiment with CNN Architecture

Create different versions of the CNN by changing its architecture.

| Experiment | Change to make |
|---|---|
| A | Increase the number of filters in the convolutional layers |
| B | Change the convolution kernel size |
| C | Add an additional convolutional layer |
| D | Change the number of units in the dense layer |

For each experiment:

1. Train the modified model.
2. Record the training and validation accuracy.
3. Record the training time.
4. Compare the results with the original model.

**Questions**

1. Which configuration achieved the best validation accuracy?
2. Did increasing the number of filters improve performance?
3. Did adding more layers always improve the results?
4. What effect did the changes have on training time?

## Task 3: Investigate Overfitting

Run the following experiments:

| Experiment | Configuration |
|---|---|
| A | Original model |
| B | Model with image augmentation |
| C | Model with image augmentation and dropout |

For each experiment:

1. Plot training and validation accuracy.
2. Plot training and validation loss.
3. Compare the differences between training and validation performance.

**Questions**

1. How can you identify overfitting from the accuracy and loss curves?
2. Did image augmentation reduce overfitting?
3. What effect did dropout have on model performance?
4. Which configuration would you recommend, and why?

## Task 4: Test the Model with New Images

1. Select several images that were not used during training.
2. Preprocess the images using the same approach as the original model.
3. Pass the images through the trained model.
4. Record the predicted class and confidence score.
5. Compare the predictions with the actual image contents.

**Questions**

1. Did the model classify all images correctly?
2. Which images were misclassified?
3. What might explain incorrect predictions?
4. How could the model be improved?

## Expected Deliverables

- Modified CNN architecture.
- Training and validation accuracy results.
- Accuracy and loss graphs.
- Predictions for unseen images.
- A short discussion of the experiments and findings.

---

# Activity 2: Video Classification Using a CNN-RNN Architecture

**Reference:** [Video Classification with a CNN-RNN Architecture – Keras](https://keras.io/examples/vision/video_classification/)

## Aim

To investigate how CNNs and Recurrent Neural Networks (RNNs) can work together to classify video sequences.

## Learning Outcomes

By the end of this lab, you should be able to:

- Explain the difference between image and video classification.
- Describe how CNNs extract features from video frames.
- Explain how an RNN models information across video frames.
- Experiment with video input and model configurations.
- Evaluate the performance of a video classification model.

## Task 1: Explore the Example

1. Open the Keras video classification example.
2. Read through the implementation.
3. Identify how video clips are processed before being passed to the model.
4. Run the example and observe the predictions.

**Questions**

1. What dataset is used in the example?
2. What is a video frame?
3. Why does the model process multiple frames rather than a single image?
4. What is the role of the CNN?
5. What is the role of the RNN/GRU?
6. Why is the order of video frames important?

## Task 2: Experiment with the Number of Video Frames

Modify the number of frames used to represent each video.

| Experiment | Number of frames |
|---|---:|
| A | 10 |
| B | 20 |
| C | 30 |

For each experiment:

1. Train the model.
2. Record training and validation accuracy.
3. Record training time.
4. Compare the results.

**Questions**

1. Does increasing the number of frames improve classification accuracy?
2. What happens to training time as the number of frames increases?
3. Why might using too few frames affect classification?
4. Is there a point where additional frames provide little benefit?

## Task 3: Experiment with the GRU Configuration

Modify the number of GRU units used in the recurrent part of the model.

| Experiment | GRU units |
|---|---:|
| A | 8 |
| B | 16 |
| C | 32 |

For each experiment:

1. Train the model.
2. Record the training and validation accuracy.
3. Compare the training time.
4. Identify the best-performing configuration.

**Questions**

1. What happens when the number of GRU units increases?
2. Does a larger GRU always produce better results?
3. How does the GRU help the model understand video sequences?
4. What is the relationship between model complexity and computational cost?

## Task 4: Compare Image and Video Classification

Use the results from Lab 1 and Lab 2 to complete the following table.

| Comparison | Image classification | Video classification |
|---|---|---|
| Input | Single image | Sequence of frames |
| Main task | Classify image content | Classify an action or event |
| CNN role | Extract image features | Extract features from video frames |
| RNN/GRU role | Not required in the basic image model | Model temporal information |
| Computational requirements | | |
| Applications | | |

**Questions**

1. What additional information can a video classifier learn compared with an image classifier?
2. Why might video classification require more computational resources?
3. Could a single image identify an action such as running or jumping reliably? Explain your answer.
4. Give two applications where video classification would be more suitable than image classification.

## Expected Deliverables

- Modified video classification model.
- Results for different frame counts.
- Results for different GRU configurations.
- A comparison of image and video classification.
- A short discussion of the experiments and findings.

---

# Activity 3: Mini-Project — Develop Your Own Classification Model

## Aim

To apply the knowledge gained from Activity 1 and 2 to develop an image or video classification application.

## Choose One Project

### Option A: Image Classification

Choose an image classification problem, such as:

- Plant or leaf disease classification.
- Waste classification (plastic, paper, metal, glass).
- Food image classification.
- Traffic sign classification.
- Animal classification.

### Option B: Video Classification

Choose a video classification problem, such as:

- Sports activity recognition.
- Human activity recognition.
- Exercise movement recognition.
- Hand gesture recognition.
- Traffic activity recognition.

## Project Tasks

### 1. Define the Problem

- Describe the classification problem.
- Identify the classes to be recognised.
- Explain a possible real-world application.

### 2. Prepare the Dataset

- Find or collect a suitable dataset.
- Organise the data into classes.
- Divide the data into training and validation sets.
- Explain any preprocessing required.

### 3. Design the Model

- Select a suitable model architecture.
- Explain the role of each major layer.
- Identify the input and output dimensions.

### 4. Train the Model

- Train your model using the selected dataset.
- Record training and validation accuracy.
- Experiment with at least two model configurations.

### 5. Evaluate the Model

- Calculate classification accuracy.
- Generate a confusion matrix.
- Test the model with previously unseen data.
- Identify examples where the model performs poorly.

### 6. Discuss Your Findings

- Explain what worked well.
- Identify limitations.
- Suggest improvements.
- Discuss potential real-world applications.

## Project Deliverables

- A working image or video classification model.
- Dataset description and preprocessing steps.
- Model architecture and implementation.
- Training and evaluation results.
- Confusion matrix.
- Demonstration using unseen data.
- A short report or presentation explaining your findings.
