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


