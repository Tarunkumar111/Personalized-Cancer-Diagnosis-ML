# Personalized-Cancer-Diagnosis
Applying various machine learning classification techniques on a dataset which contains around 3.3K datapoints of Gene ( Gene causing cancer ), Variations ( Variations in the architecture of amino acids or variations in protein-protein interactions ) and TEXT ( Medical Literature which will help in classifying the type of cancer) . Here our task is to classify the given datapoint consisting information of Gene and Variation into one of the 9 cancer classes mentioned in the dataset using medical literature 

### Case Study Explanation : 
Objective: Predict the probability of each data-point belonging to each of the nine classes.
<br>
<br>
[ 1 ] We have two files, named as 'training_variants' and 'training_text' which contains the whole dataset.
<br>
[ 2 ] Reading Dataset :- Lets read and save the data point (gene and variation data) in pandas dataframe(data_variants).
<br> Number of data points :  3321
<br> Number of features :  4
<br> Features :  ['ID' 'Gene' 'Variation' 'Class']
<ul>
<li>ID : the id of the row used to link the mutation to the clinical evidence</li>
<li>Gene : the gene where this genetic mutation is located</li>
<li>Variation : the aminoacid change for this mutations</li>
<li>Class : 1-9 the class this genetic mutation has been classified on</li>
</ul>
Lets read and save the data point (text data) in pandas dataframe(data_text).
<br> Number of data points :  3321
<br> Number of features :  2
<br> Features :  ['ID' 'TEXT']
<ul>
<li>ID : the id of the row used to link the mutation to the clinical evidence</li>
<li>TEXT : clinical evidence (text) that human experts/pathologists use to classify the genetic mutations</li>
</ul>
<br>
[ 3 ] Preprocessing of text data:-
<ul>
<li>Stopword removal using nltk library</li>
<li>Merged data_variants, data_text into one dataframe</li>
<li>Null checking using 'result[result.isnull().any(axis=1)]'</li>
<li>Filling the null data 'result.loc[result['TEXT'].isnull(),'TEXT'] = result['Gene'] +' '+result['Variation']'</li>
</ul>
<br>
[ 4 ] Data splitting:- Splitting data into train, test and cross validation (64:20:16)










