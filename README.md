# Key Recovery Side-Channel Attack Classic McEliece

This git contains the associated code of the our SAC submission.

## Requirements:
    galois, numpy

## Arguments
    The program takes as input 3 mandatory arguments and 1 optional.
* The first argument *nb_test* is the number of pairs we try to reconstruct.
* The second argument *t* is the degree of the polynomial *g*  of *Classic McEliece*.
* The third arguement *m* is the extension power of the field, *m*=9, 12 or 13.
* The fourt optional argument is the accuracy, by default set to 1. It correspond to the propoertion of faulty weight we consider in our attack.
    
## Example

    python full_attack.py 100 64 12 --accuracy 0.98
In the example: 
* m=12 means that computations take place in F_{2^{12}}
* t=64 means that the weight matrix has 128 lines
* nb_test=100 means that we try to reconstruct 100 pairs \alpha,\beta
* accuracy=0.98 means that the weight of each \alpha^i\beta (or each entry of the weight matrix) is altered as +-1 with probability 2%
