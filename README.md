Download Link: https://assignmentchef.com/product/solved-ml-homework6-adaboost
<br>
<strong>AdaBoost. </strong>In this exercise, we will implement AdaBoost and see how boosting can be applied to real-world problems. We will focus on binary sentiment analysis, the task of classifying the polarity of a given text into two classes – positive or negative. We will use movie reviews from IMDB as our data.

Download the provided files from Moodle and put them in the same directory:

<ul>

 <li>review polarity.tar.gz – a sentiment analysis dataset of movie reviews from IMBD.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>Extract its content in the same directory (with any of zip, 7z, winrar, etc.), so you will have a folder called review polarity.</li>

 <li>process data.py – code for loading and preprocessing the data.</li>

 <li>py – this is the file you will work on, change its name to adaboost.py before submitting.</li>

</ul>

The main function in adaboost.py calls the parse data method, that processes the data and represents every review as a 5000 vector <em>x</em>. The values of <em>x </em>are counts of the most common words in the dataset (excluding stopwords like “a” and “and”), in the review that <em>x </em>represents. Concretely, let <em>w</em><sub>1</sub><em>,…,w</em><sub>5000 </sub>be the most common words in the data, given a review <em>r<sub>i </sub></em>we represent it as a vector <em>x<sub>i </sub></em>∈ <em>N</em><sup>5000 </sup>where <em>x<sub>i,j </sub></em>is the number of times the word <em>w<sub>j </sub></em>appears in <em>r<sub>i</sub></em>. The method parse data returns a training data, test data and a vocabulary. The vocabulary is a dictionary that maps each index in the data to the word it represents (i.e. it maps <em>j </em>→ <em>w<sub>j</sub></em>).

(a)<strong> </strong>Implement the AdaBoost algorithm in the run adaboost function. The class of weak learners we will use is the class of hypothesis of the form:

<em> ,</em>

That is, comparing a single word count to a threshold. At each iteration, AdaBoost will select the best weak learner. Note that the labels are {−1<em>,</em>1}. Run AdaBoost for <em>T </em>= 80 iterations. Show plots for the training error and the test error of the classifier implied at each iteration <em>t</em>, <em>sign</em>(<sup>P<em>t</em></sup><em><sub>j</sub></em><sub>=1 </sub><em>α<sub>j</sub>h<sub>j</sub></em>(<em>x</em>)).

<ul>

 <li><strong> </strong>Run AdaBoost for <em>T </em>= 10 iterations. Which weak classifiers the algorithm chose? Pick 3 that you would expect to help to classify reviews and 3 that you did not expect to help, and explain possible reasons for the algorithm to choose them.</li>

 <li><strong> </strong>In next recitation you will see that AdaBoost minimizes the average exponential loss:</li>

</ul>

<em>.</em>

Run AdaBoost for <em>T </em>= 80 iterations. Show plots of <em>` </em>as a function of <em>T</em>, for the training and the test sets. Explain the behavior of the loss.

<a href="#_ftnref1" name="_ftn1">[1]</a> http://www.cs.cornell.edu/people/pabo/movie-review-data/