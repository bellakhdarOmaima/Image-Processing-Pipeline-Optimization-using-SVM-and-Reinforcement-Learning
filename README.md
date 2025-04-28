# Image Processing Pipeline Optimization using SVM and Reinforcement Learning
## Project Overview
This project focuses on optimizing an image processing pipeline to improve segmentation performance by combining classical approaches (SVM) with modern techniques (Reinforcement Learning).

## 🛠️ Project Steps
#### 1- Loading the Data

Import input images and corresponding ground truth masks from the specified folders.

#### 2- Defining Processing Pipelines

Create 8 different pipelines by combining:

   -Filtering
   -Contrast Adjustment
   -Thresholding

Each pipeline follows a specific sequence of operations.

#### 3-Initial Pipeline Evaluation

   -Apply each pipeline to all images.
   -Select the pipeline achieving the best F1-Score for each image.
   -Assign the optimal pipeline to each image based on performance.

#### 4-Feature Extraction

Extract various features from the images, such as:

   -Intensity histograms
   -Local Binary Pattern (LBP)
   -Statistical measures: noise level, average intensity, entropy

#### 4-Training the SVM Model

Use the extracted features to train an SVM model that predicts the best pipeline for new images.

#### 5-Selecting the Majority Pipeline

Identify the pipeline that is most frequently selected (majority vote) across the entire dataset.

#### 6-Reinforcement Learning Optimization

    -Develop a custom Gym environment.
    -Train a Reinforcement Learning agent to dynamically adjust the parameters of the majority pipeline.
    -Continuously improve overall performance.

#### 7-Final Evaluation

  -Apply the optimized parameters to the entire dataset.

  -Calculate the final average F1-Score.

   -Test and visualize the results on new images.

##  Technologies Used
Python 3.12

Scikit-learn: SVM, evaluation metrics

OpenCV: Image processing (filtering, thresholding, contrast adjustment)

Scikit-image: Feature extraction (LBP, histograms)

Stable-Baselines3: Reinforcement Learning

Gym: Custom RL environment creation

Matplotlib: Result visualization

## 📂 Project Structure
bash
Copy
Edit
.
├── data/
│   ├── images/
│   └── ground_truths/
├── Notebook.ipynb 
├── README.md
└── requirements.txt
###  How to Run the Project
Install the dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the main steps:

Define and apply the pipelines.

Extract features.

Train the SVM model.

Select the majority pipeline.

Train the RL agent.

Evaluate and visualize the final results.

#### 📈 Expected Results
Improved average F1-Score after optimization.

##### An adaptive pipeline capable of efficiently processing new unseen images.

#### ✨ Contributions
Contributions are welcome! Feel free to submit an issue or a pull request.
