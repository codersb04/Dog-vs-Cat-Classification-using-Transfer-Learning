# Dog-vs-Cat-Classification-using-Transfer-Learning
## Task
Build a machine learning model to classify images of Dog and Cat using Transfer Learning.</br>
Tool Used: Google Colab, Python
## Transfer Learning
Transfer Learning is a Deep Learning technique where a pre-trained model is used. This pre-trained model is trained for one task and can be re=trained for a similar task with a smaller dataset.</br>
Transfer Learning gives higher accuracy compared to training model from scratch.</br>
Some of the examples of pre-trained models are:
- VGG-16
- ResNet50
- Inceptionv3
- MobileNetV2</br></br>
In this project MobileNetV2 is used to achieve the result.
## Dataset
- Dataset is taken from Kaggle's Repository 'Dogs vs. Cats'. 
- Install the Kaggle Library
- Download the kaggle.json file from our own kaggle account
- Configure the path of kaggle.json file
- Copy the kaggle api of dog vs cat data from kaggle (https://www.kaggle.com/competitions/dogs-vs-cats/data) and include the same with code
- Extract the Compressed dataset from the zip file(loaded by Kaggle API)
- Extract the train folder data which contains all the necessary images needed for the task.
## Step Involved
### Import the Dependencies
- numpy
- Image form PIL
- matplotlib.pyplot
- matplotlib.image
- train_test_split
- cv2_imshow
### Image Processing
- Count the number of cat and dog image in the dataset
- Resize all the images to the size (224,224) as required by MobileNetV2 and storing it in a new folder
- Create the label for all the resized images of Dog and Cat
- Covert all the resized image to numpy array
- Convert the labels to numpy array
- Spilt the data into training and test data
- Scale the data to same range to ease the process by dividing it data by 255
### Building the neural netwok
- Import tensorflow and tensorflow hub
- Get the MobilNetV2 model
- Load the pretraining model with 1 output layes with number of classes
- Compile the model
- Train the Model with Training data
- Check for the accuracy for test data
  - Test Data Loss:  0.08663953095674515
  - Test Data Accuracy:  0.9674999713897705
### Building a predictive system
- get the image path as input from used
- read the image using cv2.imread
- Resize the image to (224,224) size
- Scale the image data
- reshape the data using numpy
- Feed the data to created model
- Print the result
