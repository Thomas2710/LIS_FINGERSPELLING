# 🚀 LIS Fingerspelling recognition

This repository contains teaching material that introduces students to deep learning with a practical project: recognition of alphabet gesture of the italian sign language.

## :computer: Lectures

- First Lecture: Intro to data processing
- Second Lecture: Intro to deep learning models
- Third Lecture: Recognition project + Showcasing of a more complex scenario with mediapipe

---

## 🛠️ Installation

This project uses [Poetry](https://python-poetry.org/) to manage dependencies and virtual environments. To get started:

### 1. Install Poetry

If you don’t already have Poetry installed:

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

### 2. Clone the Repository

```git clone https://github.com/Thomas2710/LIS_FINGERSPELLING.git```
```cd LIS_FINGERSPELLING```

### 3. Install the project 
```poetry install```

### 4. Usage
- ```poetry shell```
- ```cd directory_of_choice```
- ```code notebook_of_choice```
- Select lis as kernel in vscode
- Run the notebook


# :anchor: First Lecture
- __1.basic_data__ contains an introduction to numpy and pandas
- __1.basic_data_SOL__ contains the solution to the exercises in basic_data
- __2.images__ introduces to image processing techniques and how images are stored according to the most popular image processing library: __opencv__.
- __2.images_SOL__ contains the solution to the exercises in images

imgs_folder contains images used in the tutorials, feel free to add some more.

# :rotating_light: Second Lecture
- __1.discriminatore_AND__ contains a first approach to neural networks, in particular an MLP. It shows how complex and deep networks aren't always the solution, and for lower and linear problems we can also achieve explainability (plot of the line separating the samples). Teaches how to write a training loop, and what are the various elements involved in training.
- __discriminatore_AND_solution__ contains the solution to discriminatore_AND
- __2.model_testing__ let students play a bit with neural networks layers
- __3.mnist__ puts together what we learned about image processing and training a neural network, using those skills to train a classifier for the famous mnist problem
- __mnist_solution__ contains the solution to the mnist notebook

# :airplane: Third Lecture
- __1.CLIP__ contains a program that shows how most AI's nowadays work: by learning an embedding space. Play a bit with the images and text in the code to see what the AI considers to be similar :thumbsup:
- __clip_imgs__ contains the images used for the clip notebook

## 📂 Downloading the Dataset from Kaggle
The followin notebooks require a dataset hosted on [Kaggle](https://www.kaggle.com). In particular, the dataset is [LIS_FINGERSPELLING](https://www.kaggle.com/datasets/nicholasnisopoli/lisdataset).
The dataset must be downloaded and placed under __archive/LIS-fingerspelling-dataset__ as structured in this repo.

__It is important that the folder structure is the same as  in this repo__

- __2.0.train_recognition__ contains a recognition algorithm based on a CNN. Should be the same exercise as in __3.mnist__ but with a bit of additional work to do on the dataset creation. The model takes a while to create, and it saves its weights under __checkpoints/cnn/__
- __2.1.real_time_inference_cnn__ contains a real time inference using the computer internal camera. It loads the model trained in the previous notebook to perform real time recognition. It is normal to see that the performances obtained in the test set are very different from the real_time prediction
- __2.2.train_recognition_SOL__ contains the solution to 2.0.train_recognition


- __3.generate_landmark_dataset__ is a notebook that generates the data for the next notebooks. It start generating it from __archive/LIS-fingerspelling-dataset__, so it is important that the original dataset is not corrupted

- __4.0.train_landmark_recognition__ contains a recognition algorithm based on Google's mediapipe library. This library uses the positions of the hand salient points (landmarks) instead of the full image to recognize hand gestures. The notebook saves its weights under __checkpoints/landmark/__

- __4.1.real_time_inference_landmark__ contains a real time inference using the computer internal camera. It loads the model trained in the previous notebook to perform real time recognition. The performances are better than with the cnn model. Simmetry of hands is still not implemented so try to gesture with both hands

- __5.data_collection__ Finally, in this last notebook we can create our own dataset of gestures. Running the notebook will ask for which symbol you want to collect data for. Symbols are customizable in the notebook by changing the class_map dictionary. After that, camera will start recording and whenever a key is pressed, will collect a picture and save it under the right folder under __data/__.

When q is pressed, you get the possibility to change symbol. When s is pressed, the notebook stops.
__In order to succesfully press a key, you must have the focus on the camera window, not the code!!__

By iterating 5.data_collection -> 3.generate_landmark_dataset -> 4.0.train_landmark_recognition -> 4.1.real_time_inference_landmark and adjusting the data folder paths, it is possible to train a recongnition algorithm for your own images and symbols, have fun!

