# Write-a-program-to-parse-integer-n-into-prime-factors-in-Python.-Example-100-2x2x5x5
Write a program to parse integer n into prime factors in Python. Example: 100 = 2x2x5x5
"""
  * Parsing integers into prime factors
  *
  * @param PositiveInt
  * @return
"""
def phanTichSoNguyen(n):
     i = 2;
     listNumbers = [];
     # analysis
     while (n > 1):
         if (n % i == 0):
             n = int(n / i);
             listNumbers.append(i);
         else:
             i = i + 1;
     # if listNumbers is empty then add n to listNumbers
     if (len(listNumbers) == 0):
         listNumbers.append(n);
     return listNumbers;
 
n = int(input("Enter a positive integer n = "));
# parse positive integers n
listNumbers = phanTichSoNguyen(n);
size = len(listNumbers);
sb = "";
for i in range(0, size - 1):
     sb = sb + str(listNumbers[i]) + " x ";
sb = sb + str(listNumbers[size-1]);
# Print results to the screen
print("Result:", n, "=", sb);
