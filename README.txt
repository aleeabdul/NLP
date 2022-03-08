Project Title: Child Abuse Detection using Natural Language Processing (NLP)

* Platforms Needed:
1. Download Anaconda Navigator
2. Open Jupyter Notebook (Python Version: 3.0)

* How to run the code:
1. Open the file with the name "Code.ipynb".

2. Start running code cells from the start until you reach a heading
   by the name: "Preparation of Vectorized Tweets".

3. --DO NOT-- run the following cell:
 "# From the trained model, we have prepared vectorized sentences
vectored_sens = x
for i in range(vectored_sens.shape[0]):
    vectored_sens.iloc[i] = sentence_vec(vectored_sens.iloc[i],model_W2V)"

4. --RUN-- the following cell:
"#vectored_sens.to_pickle("dummy.pkl")
unpickled_df = pd.read_pickle("dummy.pkl")
print (vectored_sens[1])"

**NOTE: By following steps 4 and 5 you will save hours of processing for
	the preparation of vectorized tweets. Instead these are already
	stored in a dummy pickle file inside the repository. Which you
	will import with the help of step 4.

5. Start running code cells again from the heading by the name: "Data Spliting".

6. Stop when you reach the following cell:
"#Training 
model_FCC.fit(np.array(X_train), cat_y_train,epochs=50,verbose=1,validation_split=0.1)"

--DO NOT-- run the above described cell.

7. --RUN-- the following cell:
"#model_FCC.save_weights("Model_fcc")
tf.lite.TFLiteConverter.from_keras_model('Model_fcc')"

**NOTE: By following step 6 and 7 you will save time of training the Neural Network.
	Instead the weights have been stored in a file "Model_fcc". Which you
	will import with the help of step 7.

8. Run all the cells until you reach the last cell where you can see the program
   demands the username of the person whose tweets you need to extract. This was
   only done in order to demonstrate the working of project on live twitter data
   with the help of my account. You can edit the last part of the code according
   to your requirements as to how you want to display the starting message to the user. 