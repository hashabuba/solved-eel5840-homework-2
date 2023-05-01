Download Link: https://assignmentchef.com/product/solved-eel5840-homework-2
<br>
<h1>Question 1 –</h1>

In this homework, you will be implementing a <em>probabilistic generative classifier </em>and a <em>KNN classifier </em>and compare their results on the same data.

Three datasets for <em>training </em>are provided:

<ul>

 <li>txt has 2D data from two classes. You can visualize these data points in a scatter plot.</li>

 <li>txt has 7D data from two classes.</li>

 <li>txt is high dimensional data from five classes.</li>

</ul>

Class labels are given in the last column of all three provided training datasets.

Three unlabeled <em>testing </em>datasets are provided:

<ul>

 <li>txt</li>

 <li>txt</li>

 <li>txt)</li>

</ul>

Your goal is to discriminate among the classes in each *forTrain file, then provide a classification result for the data in each *forTest file.

Complete the following tasks:

<ol>

 <li>In your hw02.py file, submit code that implements and runs the following:

  <ul>

   <li>Implement the <em>probabilistic generative classifier</em>, under the assumption that your likelihood model <em>p</em>(<em>x</em>|<em>j</em>) is mutivariate Gaussian and the prior probabilities <em>p</em>(<em>j</em>) are dictated by the number of samples <em>n<sub>j </sub></em>∈ <em>R </em>that you have for each class. This classifier is given by comparing the posterior probability for each class <em>j</em>.</li>

  </ul></li>

</ol>

First, we assume that each class <em>j </em>can have an arbitrary mean <em>µ<sub>j </sub></em>∈ <em>R<sup>d </sup></em>and an arbitrary <em>full covariance </em>matrix <em>R<sup>d</sup></em>×<em><sup>d</sup></em>. Both of these quantities are to be estimated from the observations in each class

<ul>

 <li>Then, implement the <em>probabilistic generative classifier </em>under the assumption that your data is distributed according to a multi-variate Gaussian with a <em>diagonal covariance</em></li>

</ul>

<em>Hint: </em>A diagonal covariance implies the variables in different dimension are independent. That reduces the problem to several univariate MLE problems. The <em>diagonal covariance </em>is given as

where <em>k </em>= {1<em>,</em>2<em>,</em>··· <em>,d</em>} indicates dimension. <em>x<sup>j</sup><sub>ik </sub></em>is the <em>i<sup>th </sup></em>samples in dimension <em>k </em>from classes <em>j</em>, and <em>µ<sub>jk </sub></em>is the estimated mean in dimension <em>k </em>from classes <em>j</em>.

<ul>

 <li>Implement the <em>KNN classifier</em>.</li>

</ul>

<ol start="2">

 <li>Test your classifier implementations on the provided data set several times withdifferent parameter settings and using *cross validation*. Provide a PDF entitled hw02.pdf that discussed the following items:

  <ul>

   <li>When training the probabilistic generative classifier, how does the <em>full covariance </em>compare to <em>diagonal covariance </em>in performance for each of the data sets? Why?</li>

   <li>When training KNN classifier, what happens as you vary <em>k </em>from small to large? Why?</li>

  </ul></li>

 <li>Determine which classifier(s) you would use for each data set and give an explanationof your reasoning. <em>Hint: </em>This should incorporate some discussion based on results from cross-validation.</li>

 <li>Submit three .txt files with your predictions for the class label for each test dataset named 2DforTestLabels.txt, 7DforTestLabels.txt, and HyperSpectralforTestLabels.txt in each of the three test data sets, respectively. You should use whatever method you implemented that you believe will give the best classification results. You should generate these files by running the numpy.savetxt function on a numpy array with the class labels for each test data point in the order they appear in the</li>

</ol>

*forTest.txt files.