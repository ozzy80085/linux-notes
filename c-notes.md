format specifiers: 
---
- %d - integer
- %f - float
- %s - string
- %c - character (one letter)
---


float vs double:
-

TLDR: they both do the same thing however a double is double as precise (hence it being called double)

this defines howOld as a float and has a value of 69.420:

    float howOld = 69.420;

but when we print it:

    printf("%f", howOld);

it outputs 69.419998

but when you define it as a double instead of float 

    double howOld = 69.420;
	printf("%f", howOld);

it outputs 69.420000

data types:
--------------------------
this can only save 1 character (i have no idea why you would want to only store 1 character):

    char foo = "e";

in order to store several characters:

    char foo[] = "qwerty";

to save an int (a whole number):

    int howOld = 69;

so save a double (not a whole number):

    double howOld = 69.420;
so save a float (not a whole number):

    float howOld = 69.420;


hello world:
-------------------

    #include <stdio.h>
    
    int main() {
        printf("Hello world");
        return 0;
    }


# faq:
## why is the second word of a variable capitalized?

its called camelcase since variable names cant have spaces in them we use camelcase to improve text readability howOld is easier to read then howold
