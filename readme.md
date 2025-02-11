# Improved Model for Mathematical Expression Recognition
This project is essentially a 2.0 version of a previous project that attempted to recognize math expressions. The purpose of this project is to implement various adjustments to the previous project, each with varying levels of changes in order to improve accuracy, and also improve the usefulness of the model and the app. 

## Functions
Currently, the original model uses a simple CNN to try and break down and input image for digit and symbol recognition. The app has a simple front-end, where the user can upload an image that the model will analyze and return a result for. Plans are there to have a drawbox in place so that users can write their equations, however more work needs to be done for that to work efficiently. Once the image is uploaded, the app sends a POST method using JS that is picked up by the endpoint that the model contains using Flask. It then converts the image (which was sent as JSON) and preprocess the image before feeding it to the model and returning the output. 

## Improvements and Changes
While the model endpoints work, there is a lot of work that needs to be done so that the model can accurately evaluate the given math expression and return the correct answer.The changes to be implemented for the model are as follows:

### 1. Improved Image Preprocessing
One of the simplest changes that can be implemented is an improved system for preprocessing the incoming math expression. This means implementing a new adaptive thresholding as opposed to the current thresholding, and also a noise reduction function to help improve in low quality image settings.

### 2. Improved Digit and Symbol Recognition
The most time consuming change to the project will be creating a more complex model and system that allows for the app to recognize and solve math equations. this process involves implementing a more powerful or complex model, such as a ResNet or EfficientNet. The other potential change could be implementing a Visual Transformer (ViT), however more research has to be done to implement that. Additionally, improving the outputs recieved from the model, instead of being One-Hot Outputs, would allow for more dynamic and complex recognition.