High-Level Design (HLD) Document
Project Overview:
The Fashion Item Detection project employs the YOLO v8m.pt model, specifically utilizing the medium-sized model variant. 
The YOLO v8 architecture offers versions ranging from nano to extra-large, with the medium model chosen for this project. 
The dataset is structured within the 'data' folder, comprising three subfolders: 'train,' 'test,' and 'validation.' 
This custom dataset consists of 64 images categorized for training (44), testing (10), and validation (9) purposes.

Dataset Structure:
The project necessitates the creation of a 'data.yaml' file specifying the dataset paths for each task (train, test, validation), along with object names and their corresponding counts. 
The dataset creation process involved the utilization of the CVAT platform (https://www.cvat.ai/), facilitating project creation, image uploading, annotation, 
and dataset download in a YOLO-compatible format.

Implementation Environment:
The project can be executed using various tools, including the command line interface (CLI), Jupyter Notebook, or Google Colaboratory. 
The notebook 'AccessorySpotter_.ipynb' demonstrates the entire workflow using Jupyter Notebook. Installation of Ultralytics is a prerequisite, achieved through a simple pip statement.

Model Training:
Training involves importing the YOLO model from Ultralytics, initializing the medium-sized model, and initiating the training process. 
Post-training, the best and worst models are saved within the 'run/detect/train/weights' folder. Model validation employs the best-saved model, which is used for predicting unseen images.

GPU Acceleration:
The project supports GPU acceleration for faster computations during training and validation. 
Users with compatible GPUs should ensure upgraded GPU drivers, the correct version of CUDA, CuDNN, and TensorFlow. Reference the TensorFlow website for version compatibility.

Data Augmentation:
Data augmentation enhances model robustness. Default parameters are suitable for training, but users can experiment with additional augmentation techniques for improved results.

YOLO v8 Modes and Tasks:
The YOLO v8 model supports three modes: 'train,' 'val,' and 'predict,' each serving different tasks. For this project, the 'detect' task within the 'predict' mode is utilized for 
object detection.

Conclusion:
The provided documentation serves as a guide for understanding and replicating the Fashion Item Detection project. 
Users can refer to the 'AccessorySpotter_.ipynb' notebook for detailed explanations and the complete code implementation. 
The project emphasizes YOLO v8's versatility and its application in real-world scenarios, particularly within the realm of fashion item detection.
