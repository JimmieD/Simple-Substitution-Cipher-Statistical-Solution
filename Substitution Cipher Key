#James Dickey
#
#Letter Frequency Analysis Using Brute Force
#
#This file counts the frequency of letters in a text file.  Those letters are arranged in order of most frequent to least frequent.
#The ordered list is printed out with an assignment of each letter in the text file to it's corresponding frequency of letters used 
#in the English language.

#For example: The most frequent letter used in the text file is assigned the letter "e" which is the most frequent letter used in the 
#English language.  The second most frequent letter in the text file is assigned the letter "t" which is the 2nd most frequent letter
#used in the English language, and so on.

#The ultimate purpose is to statistically assist in solving simple substituion ciphers. See also http://www.cryptograms.org/letter-frequencies.php

fname = input('Enter a file name: ')
fh = open(fname)

alphabet = "abcdefghijklmnopqrstuvwxyz"
letter_freq = "etaoinshrdlcumwfgypbvkjxqz"
freq = list(letter_freq)
text = fh.read()

alphabet = alphabet[:26]
text = text.lower()

letter_count = {ltr: 0 for ltr in alphabet}

for char in text:
    if char in alphabet:
        letter_count[char] += 1

total = sum(letter_count.values())
i = 0

for key in sorted(letter_count, key= letter_count.get, reverse = True):
    print(key, round((letter_count[key]/total), 4), "=", freq[i])
    i = i+1


print("total:", total)
