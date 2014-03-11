
This version of Weeder supports a maximum number of 100000 input sequences. In case you want to run the program on a large set, just edit the line

MAXSEQ = 100000

in the Makefile replacing 100000 with a number large enough to accomodate all your input (but do not use insanely large numbers - it won't work, if you have 150000 sequences, write 150000!), and rebuild using make

