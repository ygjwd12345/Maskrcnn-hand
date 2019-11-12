# Maskrcnn-hand
use the model from the matterport/Mask_RCNN and train the dataset from the website http://vision.soic.indiana.edu/projects/egohands/ 
# **Color Splash Example**  
This is an example showing the use of Mask RCNN in a real application. We train the model to detect hands only, 
and then we use the generated masks to keep hands in color while changing the rest of the image to grayscale.<br>
## **Installation**  
From the Releases page page:<br><br>
1.Download mask_rcnn_coco.h5 Save it in the root directory of the repo .<br><br>
2.Download egohands_data.zip and egohands_video.zip Expand it such that it's in the path hand/.<br><br>
## **Run Jupyter notebooks**  
Open the `inspect_hand_data.ipynb` or `inspect_hand_model.ipynb` Jupter notebooks. 
You can use these notebooks to explore the dataset and run through the detection pipelie step by step.
## **Train the Hand model**  
Train a new model starting from pre-trained COCO weights<br><br>
`python3 hand.py train --dataset=/path/to/hand/dataset --weights=coco`<br><br>
Resume training a model that you had trained earlier<br><br>
`python3 hand.py train --dataset=/path/to/hand/dataset --weights=last`<br><br>
Train a new model starting from ImageNet weights<br><br>
`python3 hand.py train --dataset=/path/to/hand/dataset --weights=imagenet`<br><br>
The code in `hand.py` is set to train for 3K steps (30 epochs of 100 steps each), 
and using a batch size of 2. Update the schedule to fit your needs.
## **video** 
[video](https://youtu.be/5Q24BRIz64Q)

