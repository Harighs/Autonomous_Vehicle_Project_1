# Checking the notebooks:
Due to nature of the architecture and inbuilt dependencies of the python script providing one single jupyter notebook is not feasible. so we share our repository so that you can clone and run the code on your local machine.

1. Clone the repository using the following command
```
git clone https://github.com/Harighs/autonomous_vechicle_project_1.git
```

2. Install the required dependencies using the following command
```
pip install -r requirements.txt
```

3. Open the notebook called 'Training_Notebook.ipynb' and run the cells to train the model.
4. Trained using Nvidia 4050ti (12Gb VRAM)


# For running the training:
1. First install the required dependencies using the following command
```
pip install -r requirements.txt
```

2. Run the following command to train the model
```
python train.py --data_path <path to the data folder> --model_path <path to save the model> --batch_size <batch size> --epochs <number of epochs> 
```
eg:
```
python train.py --data data/dataset/data.yaml --cfg models/yolov5s.yaml --epochs 1 --weights '' --batch-size 32 --name repo_testing
```

# For running the Validation:
1. First install the required dependencies using the following command
```
pip install -r requirements.txt
```
2. Run the following command to validate the model
```
python val.py --data_path <path to the data folder> --model_path <path to the model> --batch_size <batch size>
```
eg:
```
python val.py --data data/dataset/data.yaml --weights runs/train/repo_testing/weights/best.pt --batch-size 32
```

