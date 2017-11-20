# Design Document for Language Project
### Jonathan Masse
### jfmasse@my.uri.edu

## Problems to solve

Milestone1:
- The amount of arguments being inputted
- Storing the trigram information
- outputting, in order, the occurrence of each trigram

Milestone2:
- The amount of arguments being inputted
- Compute and compare the frequencies of the training data files to the test data file
- Determine which training file is most similar to the test filenames
- Output the similar training file's name

## Classes needed
- Do not think I need a classes

## Other functions

- arguments2() , passed milestone2 arguments, there should be 2 or more command lines and
    return a nonzero return code if there is less than 2 arguments. The arguments
    need to be filenames or exit with a nonzero return code.
- trigram() , takes a string reference.
    - Creates a vector to store the trigram info using base 27.
    - Returns a vector of ints that the output of the vector would be
      in order from '   ' to 'zzz' the number of times each one accurse.
- similarity() , takes two vectors of ints.
    - Using for loops to calculate the similarity between the two vectors
    - Returns an int, smaller the number the more similar the two vectors are
- main() , test languageMatch.
    milestone1:
    - Create a string to test the trigram function
    - Output the vector returned by trigram(), should be 19,683 numbers (a lot of zeros)
    milestone2:
    - Read in files where the last is the test case and the rest are training data
    - All files are put through trigram()
    - Test data will be compared with each training data file in similarity
    - Outputs which language it was most similar too

## Files needed

'languageMatch.h' as public interface for languageMatch function
'languageMatch.cpp' as implentation of trigram and similarity
'main.cpp' to test languageMatch behavior

## Libraries needed

- vector
- string
- iostream
- fstream

## Compile script

- Will need to compile languageMatch.cpp and main.cpp
- Flag to skip compilation of main.cpp and produce an object file.
    milestone1 - create an executable called frequencies
    milestone2 - create an executable called language
