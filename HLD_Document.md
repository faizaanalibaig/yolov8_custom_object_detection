## High-Level Design (HLD) Document
<br>
**Project Overview:**

The Fashion Item Detection project employs the YOLO v8m.pt model, specifically utilizing the medium-sized model variant. 
The YOLO v8 architecture offers versions ranging from nano to extra-large, with the medium model chosen for this project. 
The dataset is structured within the 'data' folder, comprising three subfolders: 'train,' 'test,' and 'validation.' 
This custom dataset consists of 64 images categorized for training (44), testing (10), and validation (9) purposes.

Dataset Structure:

The project needs the creation of a 'data.yaml' file specifying the dataset paths for each task (train, test, validation), along with object names and their corresponding counts. 
This custom dataset I have created this using this website (https://www.cvat.ai/), if you want to create your own custom dataset then just open this site and click on start using CVAT after create your own project specify the name of the objects that you want to annotate and annotate your images manually after that final step download the dataset in a YOLO - compatible format. 

Implementation Environment:

The project can be executed using various tools, including the command line interface (CLI), Jupyter Notebook, or Google Colaboratory. I am using a Jupyter notebook
The notebook 'AccessorySpotter_.ipynb' demonstrates the entire workflow using Jupyter Notebook. Installation of Ultralytics is a prerequisite, achieved through a simple pip statement.

Model Training:

Training involves importing the YOLO model from Ultralytics, initializing the medium-sized model, and initiating the training process. 
Post-training, the best and worst models are saved within the weights folder and the path will be like this --> 'run/detect/train/weights'. Model validation employs the best-saved model, which is used for predicting unseen images.

GPU Acceleration:

The project supports GPU acceleration for faster computations during training and validation. 
Users with compatible GPUs should ensure upgraded GPU drivers, and users should have the correct version of CUDA, CuDNN, and TensorFlow. Reference the TensorFlow website for version compatibility. [https://www.tensorflow.org/install/source_windows#gpu]. This like is for Windows users, MacOS and Linux users can change the parameters and check their required versions on this website itself.

Data Augmentation:

Data augmentation enhances model robustness. Default parameters are suitable for training, but users can experiment with additional augmentation techniques for improved results.

YOLO v8 Modes and Tasks:

The YOLO v8 model supports three modes: 'train,' 'val,' and 'predict,' and three tasks: 'detect', 'segment', and 'classify'. For this project, the 'detect' task is used for object detection.

Conclusion:

The provided documentation serves as a guide for understanding and replicating the Fashion Item Detection project. 
Users can refer to the 'AccessorySpotter_.ipynb' notebook for detailed explanations and the complete code implementation. 
The project emphasizes YOLO v8's versatility and its application in real-world scenarios, particularly within the realm of fashion item detection.
