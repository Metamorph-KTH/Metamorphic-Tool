# Metamorphic-Tool

An oracle is used in software testing to derive the verdict (pass/fail) for a test case. Lack of precise test oracles is one of the major problems in software testing which can hinder judgements about quality. Through this research, we have created a prototype tool based on Metamorphic Testing,  which can solve both the oracle problem and the test case generation problem by testing special forms of software requirements known as Metamorphic Requirements or Metamorphic Relations(MR).

A metamorphic relation (MR) is a relation between multiple program executions that specifies how a change or transformation of the input determines a change in the output. Our tool takes the Control Flow Graphs (CFG) of an unit Java function as input and automatically outputs the MRs satisfied by that unit function using machine learning techniques and graph kernel algorithms. These predicted MRs could be later used by testers to generate new test cases and to identify faults in the program. 

The tool could also be used to train or create new models from custom Java unit function dataset. The tool uses the NetworkX library for working on the graph input and Scikit-learn library to create the machine learning models. The accuracy and efficiency of the machine learning models are visualized using the Matplotlib library. 

----------------------
Code Functionalities
----------------------
createPickle.py: Takes the Dot files and their corresponding class labels of a corresponding MR as input and generates a graph pickle object out of it. This graph pickle could be loaded by other programs for applying graph algorithms on it.

get_ROC-py: Takes the graph pickle as input and perform graph ML algorihtms on it to classiyfing it to its MR class. Later it provides a ROC metric containing the classifier accuracy details.

my_functions.py: Used to calculate the Random Walk Kernel (RWK) between two graphs.
