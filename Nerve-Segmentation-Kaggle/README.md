## Deep Learning Model for Kaggle Ultrasound Nerve Segmentation
### Overview
The task in this competition is to segment a collection of nerves called the Brachial Plexus (BP) in ultrasound images. You are provided with a large training set of images where the nerve has been manually annotated by humans. 
Annotators were trained by experts and instructed to annotate images where they felt confident about the existence of the BP landmark.
The proposed model achieved leaderboard score of ~0.58.

### Pre-processing steps
- Read all the train ultrasound photos
- Read all the mask segmentation photos (train)
- Read all the test ultrasound photos
- Resize the data, both train and test to 98*98 photos
- Normalizing the train data by centering and scaling.

### Model
The model is based on the model which I postet on [this repository](https://github.com/AvivSham/Image-Segmentation/tree/master/Unet_Model_Function).
The U-net is convolutional network architecture (auto-encoder) for fast and precise segmentation of images. There is few changes between the current model and the suggested model in my other repository:
1) The input shape is 98*98
2) In the decoder part I used ConvTranspose2D instead of Upsampling2D + Conv2D

### Instructions
- You can run the whole code in google colab using free GPU power
- Generate Kaggle's API token and upload it in the first code cell it provides you the direct access to kaggle's data
- The predicted photos are automatically saved and can be downloaded
