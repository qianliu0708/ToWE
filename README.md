# ToWE
Task-oriented Word Embedding

This software implements the task-oriented word embedding for text classification.
------------------------------------------------------
Installation
type make

Example
The example file of domain specific words is provided in "domainwords.txt". 

To run:

./towe -train 5groupcorpus -output output.txt -cbow 1 -size 300  -negative 25 -hs 1 -sample 1e-4 -threads 30 -binary 0 -iter 20 -alpha2 0.1 -beta 0.1 -group_count 50 -list domainwords.txt

Here,
-train is the training corpus

-group_count is the size of random sample for constructing the word-pairs of salient word (detailed in equation 3 in the paper).

-alpha2 is the learning rate of the function-aware component

-beta is the combination parameter (denoted as lambda in the paper)

-list is the file of domain specific words, where each line contains salient words for one category.

The learnt word embedding will be written to output.txt, specified by -output.
