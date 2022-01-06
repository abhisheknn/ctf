
**Problem statement :**

I wonder what this really is... enc ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

The given file enc have chinese characters and python code is given
From the code I got we can fairly assume that the given sting is encrypted using above code 

**Wrong Approach :**

I missed that ord() accepts unicode and returns codepoint not decimal value . 


**Correct Approach** 
   1. use any online encoder convert unicode char to codepoints 

       [28777 25455 17236 18043 12598 24418 26996 29535 26990 29556 13108 25695 28518 24376 24368 13411 12343 13872 25725] 
   2. now we know first two letters 'p' and 'i' of flag , (ord('p') >> 8) + ord(i) == 28777
   3. use bruteforce to comeup with characters

**Another Approach**

1. https://gchq.github.io/CyberChef/
2. magic recipe 
3. feed the string 