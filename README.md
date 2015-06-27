# Unsupervised Learning of PCFGs

Unsupervised Learning of Probabilistic Context Free Grammars for Event Recognition

Project: [Noptilus](http://www.noptilus-fp7.eu)<br>
Author: Nikolaos Kofinas<br>
Year: 2014<br>
Institution: School of ECE, Technical University of Crete, Greece

### Compile

To compile, issue *make* into the main folder and also inside the folder "Inside-Outside"

### Run

To run, issue the following in the command line: 

```
./PCFG-learner -d dirPath [-l learnFile.csv]+ [-t testFile.csv]+ -e [evalFile.csv]+ -f outFile 
               -w wordSize -p mode -s symbols -L normalization
```

#### Input

```
* dirPath       : The path to the directory with all input and output files
* learnFile.csv : A csv file containing the learning data
* testFile.csv  : A csv file containing the test data
* evalFile.csv  : A csv file containing the evaluation data
* outFile       : The prefix to all output files
* wordSize      : A positive integer indicating the nominal word length
* mode          : Mode of word formation for parsing a stream of symbols:
                     0 -> standard fixed nominal length
                     1 -> uniform distribution around nominal length
                     2 -> normal distribution around nominal length 
* symbols       : The number of symbols used for quantization
* normalization : The value of the normalization (lambda) parameter (typical: 0.005)
```

All the above inputs are necessary!

To set the size of the beam, change "\_beamDepth_" inside "BeamSearch/BeamSearch.hpp"

### Credits

The original code for the inside-outside algorithm can be found [here](http://web.mit.edu/course/6/6.863/python/nltk_contrib_backup/mit/six863/rr4/inside-outside/)
