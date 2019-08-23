from math import *
import sys
import time


# Euclid algorithm non recursive
def egcd_loop(x, y, verbose=False):
    if x < y: # We want x >= y
        return egcd_loop(y, x, verbose)
    while y != 0:
        (x, y) = (y, x % y)
    
    #if verbose: print('gcd is %s' % x) 
    return x

# Euclid algorithm recursive
def egcd_recur(a, b):
    if b > a:
        return egcd_recur(b, a)

    if a % b == 0:
        return b

    return egcd_recur(b, a % b)  

# Compute the GCD of 2 positive integers using Euclid's
# algorithm in a loop and using recursion and compare the
# execution times.
if __name__ == '__main__':
    t1 = time.time()
    gcd = egcd_loop(abs(int(sys.argv[1])), abs(int(sys.argv[2])))
    t2 = time.time()
    print("Time to GCD(loop)    {}: {} us".format(gcd, int(round((t2-t1)*1000000))))

    t1 = time.time()
    gcd = egcd_recur(abs(int(sys.argv[1])), abs(int(sys.argv[2])))
    t2 = time.time()
    print("Time to GCD(recurse) {}: {} us".format(gcd, int(round((t2-t1)*1000000))))
