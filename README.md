# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import math
# Probabilities given
p = [0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [3, 4, 2, 4, 3, 3, 2]
n = len(p)
# Average Codeword Length
L = sum(p[k] * lk[k] 
for k in range(n))
# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))hs = round(hs, 3)
# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)
# Variance of codeword length
var = sum((p[k]) * (lk[k]) - L) ** 2 
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

![WhatsApp Image 2025-09-14 at 11 05 15_13bae795](https://github.com/user-attachments/assets/27b5e1a8-b567-4e3a-bec3-f669dda9aa56)

# Output

<img width="500" height="200" alt="Screenshot 2025-09-13 152747" src="https://github.com/user-attachments/assets/148467ed-5bfb-4056-90b8-572dc7ddf560" />

# Results:

Huffman and Shannon-Fano coding methods were implemented on the provided source. Calculations for average codeword length, entropy, variance, redundancy, and coding efficiency have been carried out successfully
