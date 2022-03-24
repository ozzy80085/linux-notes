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

## operators

    operator | example | same as
        =       x = 5    x = 5
        +=      x += 7   x = x + 7
        -=      x -= 2   x = x - 2
        *=      x *= 3   x = x * 3
        /=      x /= 3   x = x / 3
        (these are the most common but not all)
 
 ## if else

    if  (condition) {  
	// block of code to be executed if the condition is true  
	} 
	
	else {  
	// block of code to be executed if the condition is false  
	}
---
    int time = 20;  
	
	if (time < 18) {  
		printf("Good day.");  
	} 
	
	else {  
		printf("Good evening.");  
	}

## while loop

    while (condition) {  
	// code block to be executed
	}
---
	int i = 0
	while (i < 5) {
		printf("Hello World!\n");
	}


you could also use while(1) instead 

---
## modify strings

    char greetings[] = "Tello World!";  
	greetings[0] = 'H';  
	printf("%s", greetings);
	//outputs Hello World!

## cool built in functions

    char greetings[] = "Hello World!";
	printf("%lu\n", sizeof(greetings));
	//outputs 13

hello world:
-------------------

    #include <stdio.h>
    
    int main() {
        printf("Hello world");
        return 0;
    }

## user input

    // Create an integer variable that will store the numbe get from the user  
	int myNum;  
  
	// Ask the user to type a number  
	printf("Type a number: \n");  
  
	// Get and save the number the user types  
	scanf("%d", &myNum);  
  
	// Output the number the user typed  
	printf("Your number is: %d", myNum);

a string is a little bit different

	// Create a string  
	char firstName[30];  
  
	// Ask the user to input some text  
	printf("Enter your first name: \n");  
  
	// Get and save the text  
	scanf("%s", firstName);  
  
	// Output the text  
	printf("Hello %s.", firstName);
Note that you must specify the size of the string/array (we used a very high number, 30, but atleast then we are certain it will store enough characters for the first name).

## memory addresses

    int myAge = 43;  
	printf("%p", &myAge); // Outputs 0x7ffe5367e044
your memory address will be different

## pointers
a pointer is a variable whose value is the address of another variable

    int myAge = 43; // An int variable  
	int* ptr =  &myAge;  // A pointer variable, with the name ptr, that stores the address of myAge  
  
	// Output the value of myAge (43)  
	printf("%d\n", myAge);  
  
	// Output the memory address of myAge (0x7ffe5367e044)  
	printf("%p\n", &myAge);  
  
	// Output the memory address of myAge with the pointer (0x7ffe5367e044)  
	printf("%p\n", ptr);

# faq:
## why is the second word of a variable capitalized?

its called camelcase since variable names cant have spaces in them we use camelcase to improve text readability howOld is easier to read then howold

## why is the printf statement printing on the same line
because printf doesn't automatically add a newline character
you can add a newline character with \n

    printf("Hello World!\n");
