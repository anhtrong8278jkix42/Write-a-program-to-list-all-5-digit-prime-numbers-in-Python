# Write-a-program-to-list-all-5-digit-prime-numbers-in-Python
Write a program to list all 5 digit prime numbers in Python
import math
 
"""
  * check the original
  *
  * @author viettuts.vn
  * @param n: so nguyen duong
  * @return true is so nguyen so,
  * false is not original
"""
def isPrimeNumber(n):
     # n < 2 does not have to be a prime
     if (n < 2):
         return False;
 
     # check so nguyen to when n >= 2
     squareRoot = int(math.sqrt(n));
     for i in range(2, squareRoot + 1):
         if (n % i == 0):
             return False;
     return True;
 
print("List all 5-digit primes:");
dem = 0;
for i in range(10001, 99999):
     if (isPrimeNumber(i)):
         print(i);
         dem = dem + 1;
print("The sum of 5 digit prime numbers is:", dem);
