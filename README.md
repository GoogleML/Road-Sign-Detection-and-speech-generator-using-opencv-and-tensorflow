<!DOCTYPE html>
<html lang="en-us">
  <head>
    <meta charset="UTF-8">
    <title>Road-sign-detection-and-speech-generator-using-opencv-and-tensorflow by amiteshmahajan</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="stylesheets/normalize.css" media="screen">
    <link href='https://fonts.googleapis.com/css?family=Open+Sans:400,700' rel='stylesheet' type='text/css'>
    <link rel="stylesheet" type="text/css" href="stylesheets/stylesheet.css" media="screen">
    <link rel="stylesheet" type="text/css" href="stylesheets/github-light.css" media="screen">
  </head>
  <body>
    <section class="page-header">
      <h1 class="project-name">Road-sign-detection-and-speech-generator-using-opencv-and-tensorflow</h1>
      <h2 class="project-tagline">Road Sign Detection and speech generator using opencv and tensorflow</h2>
      <a href="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow" class="btn">View on GitHub</a>
      <a href="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/zipball/master" class="btn">Download .zip</a>
      <a href="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/tarball/master" class="btn">Download .tar.gz</a>
    </section>

    <section class="main-content">
      <h1>
<a id="abstract" class="anchor" href="#abstract" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Abstract</h1>

<p><strong>Road sign detection</strong> is a very critical and trending concept for autonomous vehicles. The creation of an intelligent system to detect the road signs and convert them to speech commands can be the integral part of such autonomous vehicles in very near future.This paper presents a study to recognize traffic sign patterns using Neural Networks technique. The images are pre-processed with several image processing techniques, such as threshold techniques, Gaussian filter, Canny edge detection, Contour and Fit Ellipse. Then, the Neural Networks stages are performed to recognize the traffic sign patterns.</p>

<p>High-level architecture of the system:</p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%203.png?raw=true" alt="Image 3"></p>

<h1>
<a id="method" class="anchor" href="#method" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Method</h1>

<p>The first step of the preprocessing is to adjust the image size, reducing the space occupied when the resolution of the input image is too high. If the image size were too high, it would slow down the execution of the algorithms to the point that it would restrict the program execution. The next step is to transform the input image into a gray scale image, so the edge detection algorithm can be applied .The algorithm used to detect edges in the image is the Canny Edge Detection, which takes a grayscale image as input and produces another grayscale image as output, where only the edges are shown. Then, Morphological Operations such as dilation and erosion are applied. After this, Region of Interests or Contours are identified to locate the subject i.e. traffic sign (Rectangle, Triangle, Circle, Inverted Triangle). There are many types of traffic signs, but their shapes are very limited and characteristic, so knowing the shape allows us to determine if an ROI contains a potential traffic sign or not.</p>

<p>The Convolutional Neural Network (CNN) is a deep learning approach that stacks several convolutional, subsampling and non-linear activation layers in sequence. Recently, the CNN has become a breakthrough technique in the field of artificial intelligence for object classification and pattern recognition applications such as handwritten digit recognition, speech recognition, object classification, and face identification. A fully trainable Convolutional Neural Network (CNN) is used for the detection and recognition of traffic signs.</p>

<p>Image pre-processing steps:</p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%202.png?raw=true" alt="Image 3"></p>

<p>The following graph shows to what extent classifier is able to
correctly classify the traffic sign from a given set of classes
of traffic sign dataset:</p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%204.png?raw=true" alt="Image 3"></p>

<p>The graph shows to what extent validator is able to
accurately predict the traffic sign from a given set of classes
of traffic sign data-set:</p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%208.png?raw=true" alt="Image 3"></p>

<p>The first layers of the network C1 up to S2 function as a trainable feature extractor. All the network layers contain neuron models as in a classical Multi-Layer Perceptron (MLP) network. The feature extraction layers C1 up to S2 have specific constraints such as local connectivity and weight sharing. With these constraints, the first layers are able to extract position invariant features from two-dimensional shapes. The classification layers n1 and n2 at the output are fully connected MLPs. These layers use the extracted local features to perform classification of the input image. The details of the three different types of layers are described in the next subsections.</p>

<h1>
<a id="result" class="anchor" href="#result" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Result</h1>

<p>The Belgian Traffic Sign Dataset is used for this project, it has two directories:\
1.BelgiumTSC Training (171.3MB) - contains about  4000 images.\
2.BelgiumTSC Testing (76.5MBytes) - contains around 100 real images.\ </p>

<p>Each of the two directories above has 62 sub-directories named sequentially from 00000 to 00062. The directory name represents the code (or label) and the images inside the directory are examples of that label.</p>

<p>After completion of building this system, the system was able to correctly identify the traffic signals. To  determine the accuracy of the classifier, a graph of all the predicted images and compared it with the images used for training was generated.
The speed sign recognition application is trained with greyscale images to classify speed signs based on their shape of at least 32x32 pixel values. The exploration resulted in an efficient network architecture which has very good recognition accuracy.</p>

<p>Ground truth and prediction comparison result for 10
random images: </p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%207.png?raw=true" alt="Image 3"></p>

<p>Loss function Gradient vs the percentage of training
finished:
<img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%209.png?raw=true" alt="Image 3"></p>

<p>Figure depicting optimal resolution vs accuracy :</p>

<p><img src="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow/blob/gh-pages/fig%2010.png?raw=true" alt="Image 3"></p>

<p>One observation derived from experimenting with the resolution of the test images was that on reducing the resolution of images by half, the system find it difficult to identify the sign board in the test image. The minimum resolution at which the system is able to correctly identify the signs is found to be 32 x 32.</p>

<h1>
<a id="conclusion" class="anchor" href="#conclusion" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>conclusion</h1>

<p>This project implements a road sign board detection and recognition system based on a fully trainable Convolutional Neural Network (CNN) (TensorFlow). To train the application a dataset containing around 4500 real sign board images from Belgium are collected. The dataset is completed with 2904 background images of other road signs, the cars and other non-speed sign images. The speed sign recognition application is trained with greyscale images to classify speed signs based on their shape of at least 32x32 pixel values. The exploration resulted in an efficient network architecture which has very good recognition accuracy.
The optimal resolution was found to be 32 x 32. </p>

<h3>
<a id="authors-and-contributors" class="anchor" href="#authors-and-contributors" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Authors and Contributors</h3>

<p>Authors: <a href="https://github.com/amiteshmahajan" class="user-mention">@amiteshmahajan</a> and <a href="https://github.com/vaibhavsahu" class="user-mention">@vaibhavsahu</a>.</p>

<h3>
<a id="support-or-contact" class="anchor" href="#support-or-contact" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Support or Contact</h3>

<p>Having trouble with Pages? Check out our <a href="https://help.github.com/pages">documentation</a> or <a href="https://github.com/contact">contact support</a> and we’ll help you sort it out.</p>

      <footer class="site-footer">
        <span class="site-footer-owner"><a href="https://github.com/amiteshmahajan/Road-Sign-Detection-and-speech-generator-using-opencv-and-tensorflow">Road-sign-detection-and-speech-generator-using-opencv-and-tensorflow</a> is maintained by <a href="https://github.com/amiteshmahajan">amiteshmahajan</a>.</span>

        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a> using the <a href="https://github.com/jasonlong/cayman-theme">Cayman theme</a> by <a href="https://twitter.com/jasonlong">Jason Long</a>.</span>
      </footer>

    </section>

  
  </body>
</html>
