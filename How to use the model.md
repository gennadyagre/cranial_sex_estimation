### 1. Content of this site

***Attribute description.pdf*** – description of the cranial measurements that are used for learning the models as well as the cranial landmarks.

***SVM model.pck*** – executable Orange SVM model for sex estimating using full set (86 atts.) of cranial measurements.

***SVM classified test data.arff***  - an example of .arff file with 6 classified examples that can be used for testing the SVM model. The file can be inspected and changed by mean of an arbitrary text editor.

***SVM unclassified test data.arff***  - an example of .arff file with 6 unclassified examples that can be used for testing the SVM model. The file can be inspected and changed by mean of an arbitrary text editor.

***LR model.pck*** – executable Orange LR model for sex estimating using a subset (18 atts.) of cranial measurements.

***LR classified test data.arff***  - an example of .arff file with 6 classified examples that can be used for testing the LR model. The file can be inspected and changed by mean of an arbitrary text editor.

***LR unclassified test data.arff***  - an example of .arff file with 6 unclassified examples that can be used for testing the SVM model. The file can be inspected and changed by mean of an arbitrary text editor.

***Testing models.ows*** – an example of .ows file that can be used for testing the models in the Orange 2.7 environment

### 2. How to prepare your own test data for sex evaluation by the SVM or LR models

***2.1. Preparation of test data for evaluating by SVM model***
 
- Open file *SVM classified test data.arff* (if your test data is classified) or *SVM unclassified test data.arff* (if your test data is not classified) by means of a text editor (e.g. *Notepad*). The upper part of  the file presents the names of attributes to be used, their types (numeric) and order as well as coding of the target attribute – *sex (0 – female, 1 – male)*.
- Create an Excel table with the names of columns corresponding to the names of the attributes preserving attribute types and order.
- Fill the table with your test data – each row of the table corresponds to an example. If a test example is not classified – put ? in the corresponding cell of the “sex” column. The same symbol may be used as a value for any attribute if its real value is unknown.
- Save your data as a .csv file.
- Open your .csv file with a text editor.
- Copy all data in the file and put it in to the corresponding .arff file replacing the existing data (located after *@data* header)
- Save your .arff file

***2.2. Preparation of test data for evaluating by LR model***
- Open *LR classified test data.arff* (if your test data is classified) or *SVM unclassified test data.arff* (if your test data is not classified) by means of a text editor. The upper part of  the file presents the names of attributes to be used, their types (numeric) and order as well as coding of the target attribute – *sex (0 – female, 1 – male)*.
- Follow the instructions described in the previous section.

### 3.  How to use the models for evaluating your test data

***The models are created in Orange 2.7 data mining graphical environment (Version 2.7.8) so you need this environment to use these models.***

1.	Run the *Orange*
2.	Select option *Open* in menu *File*
3.	Select file *Testing models.ows*
4.	Open widget *File* (from the right-click menu) and select your .arff file with the prepared test data
5.	Open widget *Load Classifier* (from the right-click menu) and select the desired model (*SVM model.pck* or *LR model.pck*). 
6.	Start evaluation of your test data by selecting *Open* option from right-click menu of *Predictions* widget.
