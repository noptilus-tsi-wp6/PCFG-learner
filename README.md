# Unsupervised Learning of PCFGs

Title: Unsupervised Learning of Probabilistic Context Free Grammars for Event Recognition over Data Streams
Project: European FP7 [Project Noptilus](http://www.noptilus-fp7.eu)
Author: Nikolaos Kofinas (Graduate Student)
Year: 2014
Institution: School of ECE, Technical University of Crete, Greece

### Compile

* In order to compile this code you must run *make* into the main folder and also inside the folder "Inside-Outside"

### Run

    ./CFG-learner -d DIR_PATH [-l FILE1.csv]+ [-t FILE2.csv]+ -e [FILE3.csv]+ -f FILE4 -p SPLIT -w WORD_SIZE -s SYMBOLS -L LAMBDA

#### Input

```
1. DIR_PATH : the path to the directory that contains input files and where the output is written
2. FILE1.csv: A csv file containing the learning data
3. FILE2.csv: A csv file containing the test data
4. FILE3.csv: A csv file containing the evaluation data
5. SPLIT    : This value specifies the split method that the learner will use:
		a. 0 -> Use the standard split method
		b. 0 -> Use the uniform split method
		c. 0 -> Use the normal split method 
6. WORD_SIZE: This value defines the mean size of the generated words (coming from the quantizer)
7. SYMBOLS  : This value defines how many symbols will be used for quantization
8. LAMBDA   : This value defines the lambda parameter of the learning algorithm (typical: 0.005)
```

All the above inputs are necessary!

To change the size of the beam set the value of the "\_beamDepth_" in "BeamSearch/BeamSearch.hpp" to the desired value.

### Credits
1. The original code for the inside-outside algorithm can be found [here](http://web.mit.edu/course/6/6.863/python/nltk_contrib_backup/mit/six863/rr4/inside-outside/)
