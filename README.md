# Fake-News-Classification-using-LSTM
In the new age of technology, we go through lot of news and there is a possibility that the news could be fake. We trained a model which will help us to classify whether the news is genuine or fake. We trained the model using dataset available from Kaggle. This is a binary classification problem and we used LSTM to train the model. The model achieved good accuracy and can be worked upon to even improve it and use it in real-time.

Dataset Description:
We have appropriate the data from kaggle website refer this link https://www.kaggle.com/c/fake-news

train.csv: A full training dataset with the following attributes:
•	id: unique id for a news article
•	title: the title of a news article
•	author: author of the news article
•	text: the text of the article; could be incomplete
•	label: a label that marks the article as potentially unreliable
o	1: unreliable
o	0: reliable

Algorithm Description:
LSTM:
If you want to predict the next word for the sentence “I like numbers, my favorite subject is …” your answer would be “mathematics”. How do you come to that conclusion, it is because of the word “numbers”. Recurrent Neural Networks help us achieve this. They are neural networks with loops, allowing the information to stay for some time.
 ![image](https://user-images.githubusercontent.com/88571564/180368044-dbdde927-4bf3-433f-abe3-21d919b42cb9.png)

Figure 1: Recurrent Neural Network
Xt is the input, the Network analyzes and throws out output ht. RNNs have performed decently but the problem comes when the sentence is too long and has immense data. E.g. predict the next word for the sentence “I like numbers, my favorite subject is mathematics. My brother likes space and technology, his favorite subject is ….” your answer would be “astronomy”. How do you come to that conclusion, it is because of the word “space and technology”.
But how does the network know that word mathematics is not important now and “space and technology is important now”. Also the problem with RNNs is it cannot remember the entire sequence for long. Long Short Term Networks (LSTMs) are a special kind of RNN which are very much capable of handling long term dependencies. LSTMs has a cell state which holds the important word/information required for processing. The information in the cell state can be forgotten (removed) or added based on gates. It has 3 gates to help it decide:
1.	Forget gate: To forget the information in the cell state. Done with the help of a sigmoid function which returns a value between 0 and 1. If 1 or closer to 1, remove the word else retain the word.  
2.	Input gate: What input should be given to the cell state done with the help of tan-h function. 
3.	Update gate: Any information that can be added to the cell state. E.g. : When “space” was in cell state, update it with the word “technology” because word “technology” is important in decision making as well .
 ![image](https://user-images.githubusercontent.com/88571564/180368063-78326934-a189-4f86-a0c5-b07b5f69c0ea.png)

To get a clear understanding of LSTM along with mathematical insights, refer to this article https://colah.github.io/posts/2015-08-Understanding-LSTMs/

How to Execute?
So, before execution we have some pre-requisites that we need to download or install i.e., anaconda environment, python and a code editor. Anaconda: Anaconda is like a package of libraries and offers a great deal of information which allows a data engineer to create multiple environments and install required libraries easy and neat.
To check on how to install anaconda environment, set up jupyter notebook refer to this article. You can skip the article if you have knowledge of installing anaconda, setting up environment and installing requirements.txt
1.	Install necessary libraries from requirements.txt file provided.
 
2.	Go to the directory where your requirement.txt file is present.
<<directory of your file>>: . E.g, If my file is in d drive, then 
1.  d:
2.  cd d:\License-Plate-Recognition-main    #CHANGE PATH AS PER YOUR PROJECT, THIS IS JUST AN EXAMPLE
If your project is in c drive, you can ignore step 1 and go with step 2.
Eg. cd C:\Users\Hi\License-Plate-Recognition-main #CHANGE PATH AS PER YOUR PROJECT, THIS IS JUST AN EXAMPLE
 
3.	Run command pip install -r requirements.txt or conda install requirements.txt (Requirements.txt is a text file consisting of all the necessary libraries required for executing this python file. If it gives any error while installing libraries, you might need to install them individually

 
All the necessary files will get downloaded. To run the code, open anaconda prompt. Go to virtual environment if created or operate from the base itself and start jupyter notebook, open folder where your code is present.
 

 
Open “FakeNewsClassifierUsingLSTM,naivesbayes.ipynb” to get the results.

Results:
 ![image](https://user-images.githubusercontent.com/88571564/180368097-dfbe0fd4-b850-42e8-b5b0-b3793bfc5783.png)
![image](https://user-images.githubusercontent.com/88571564/180368116-50c2f2db-c33d-4737-a011-68e2b4cbe93f.png)




 
