# Leetcode-3110.-Score-of-a-String
Finding the sum of a string 

You are given a string s. The score of a string is defined as the sum of the absolute difference between the ASCII values of adjacent characters.

Return the score of s.

ASCII TABLE FROM a to Z :
Character	ASCII Value
a	97
b	98
c	99
d	100
e	101
f	102
g	103
h	104
i	105
j	106
k	107
l	108
m	109
n	110
o	111
p	112
q	113
r	114
s	115
t	116
u	117
v	118
w	119
x	120
y	121
z	122


# Solution:
In this problem we have to fid the score of a string by finding the absolute difference between the adjacent ascii values of alphabets 
If we have "zaz" as an example , the score of this string would be the following:
ASCII VALUE OF z= 122
ASCII VALUE OF a= 97

(|122-97| + |97-122| ) = 25+25 =50
Hence the value or score of the gven string is 50

# Code :
C++ :
class Solution {
public:
    int scoreOfString(string s) {
        int arr=0;
        for(int i= 0;i < s.size()-1;i++){
            arr+=abs(s[i]-s[i+1]);

        }
        return arr;
    }
};

1. Create a variable named arr and initiliase its value as 0 . This variable will store the result.
2. Now apply a for loop from 0 index to second last index
3. Keep on adding to the arr variable ,  the abs difference value of the current letter and next letter until the loop ends .
4. Return the value of arr
