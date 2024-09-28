# Boston Housing Price Prediction using Neural Networks
![image](https://miro.medium.com/max/888/1*guak1sQTh5sAf46NMzbQig.jpeg)
This project demonstrates the implementation of a simple neural network in Keras to predict housing prices from the **Boston Housing Dataset** using a single feature: the average number of rooms. The goal is to train a neural network to estimate the median home price based on this single feature.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training Results](#training-results)
- [License](#license)

## Project Overview

This repository implements a simple linear regression model using a neural network to predict the median home price (in $1000) based on the average number of rooms in a house. The network is trained on the **Boston Housing Dataset**, and the key steps include:
- Dataset exploration and visualization
- Defining and compiling the model in Keras
- Training the model using Mean Squared Error (MSE) loss
- Evaluating the model performance

## Dataset

The **Boston Housing Dataset** is provided by Keras and contains 13 features for each house and a target value representing the median price of homes in Boston. In this project, we use only one feature: the average number of rooms.

Features:
- **Average number of rooms** (used as the input feature)
  
Target:
- **Median house price** (used as the target output)
