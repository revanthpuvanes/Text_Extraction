# Text Extraction from images

Text extraction has major aspects in modern industry where it is helpful for wide range of domains.

One of the most popular text extraction tools are 
  - Tesseract OCR (Optimal Character Recognization)

But it do comes with the limitations, where it needs 
  - Structured text format
  - Not works well with hand written text.
  - Also text alignment need to be horizontal.

Let's see some example

![advantage](https://user-images.githubusercontent.com/80465899/148056935-1e20643a-cd0d-45e9-8950-f6493c5e6495.png)

After passing it to the OCR

![Screenshot (22)](https://user-images.githubusercontent.com/80465899/148057276-b0032f65-7f0e-4d85-adde-fc0692db95c3.png)

Well its working fine as the text in the image has its format.

Lets try with some harder image like this

![3](https://user-images.githubusercontent.com/80465899/148059834-352e541b-0716-4a4a-ad86-71ac892c29fb.jpg)

Oops! the OCR couldn't able to find any text from the above image.

Is that everything?

Really no, lets see some modern technique which uses deep learning.

# Text Detection using pre-trained model

  - East model
  - East --> Efficient and Accurate Scene Text Detector

# Workflow
  - The convolution neural network extracts features from the input image(text detected region)
  - The deep bidirectional recurrent neural network predicts label sequence with some relation between the characters.
  - The transcription layer converts the per-frame made by RNN into a label sequence.

After passing the harder image through our EAST model we get 

![Screenshot (23)](https://user-images.githubusercontent.com/80465899/148060748-933bfa8b-1e01-4b2b-9e0b-ae9629dcac96.png)

# Requirements

  - OpenCV
  - Numpy
  - Pytesseract
  - Matplotlib
  - imutils

Or you can download the pre-trained model using below link
https://raw.githubusercontent.com/oyyd/frozen_east_text_detection.pb/master/frozen_east_text_detection.pb

