                                            		C(mid-level-language)


#_What is software?
Software is a collection of programs.

#_What is a program?
The program is a collection of instructions.

#_Work of compiler?
Translates code into machine language (binary).
 	!*Advantages: Faster execution (code is already in machine code).
 	!*Disadvantages: Even one error stops compilation.

#_Work of interpreter?
Translates code line by line during execution.
 	!*Advantages: No need to compile the whole code.
 	!*Disadvantages: Needs the interpreter installed to run.

#_What are identifiers?
Identifiers are used to identify the variables, function, or other program elements.
 	e.g. = int count;  -> Here, count is the identifier.

#_Keywords: Keywords are reserved words in C that have special meaning to the compiler.(32)

			auto    |double  |int     |struct  
			--------+--------+--------+--------
			break   |else    |long    |switch  
			--------+--------+--------+--------
			case    |Enum    |register|typedef 
			--------+--------+--------+--------
			char    |extern  |return  |union   
			--------+--------+--------+--------
			const   |float   |short   |unsigned
			--------+--------+--------+--------
			continue|for     |signed  |void    
			--------+--------+--------+--------
			default |goto    |size of |volatile
			--------+--------+--------+--------
			do      |it      |static  |while   
			
#_Data Types:
 Data types define the type of data where a variable can store.
		1. Primitive: it stores simple value and its value stored directly in memory.
 	   		e.g. = int, char, float, double
 				(i)   singed  - it can store both positive and negative values.
 				(ii) unsinged - it can store only zero and positive.
 		2. Non-primitive: it stores multiple values and stores an address in memory, actually includes						       Derived Enumeration.
 				(i)  Derived:    it can store multiple values.
 					e.g. = array, pointer, structure, union
 				(ii) Enumeration: A user-defined data type used to name integer constants.
					e.g. = enum
 		3. Void: A function that doesn’t return anything
 			e.g. = void main();

			char    |1(in bytes)
			--------+-----------
			short   |2          
			--------+-----------
			int     |4          
			--------+-----------
			long    |4          
			--------+-----------
			longlong|8          
			--------+-----------
			float   |4          
			--------+-----------
			double  |8          
			--------+-----------
			long -  |8/16(varies
			 double |bycompiler)
			
#_What is Type Modifiers:
 Type modifiers are keywords that change the size or range of a data type in C.
 		e.g. = short int, long int, signed int, unsigned int, long double,unsigned char.

#_What is Type casting?
converting one data type into another.

 		1. Implicit: implicit means automatic type conversion done by the compiler.
 			e.g. = int a = 5; (A casting from a smaller data type to a larger data type.)
 			          float b = a;   // int automatically converted to float
 		2. Explicit: explicit means manual type conversion done by the programmer.
 			e.g. = float a = 5.5; (A casting from a larger data type to a smaller data type.)
 			          int b = (int)a;   // float manually converted to int

#_Operators:
 	1. Arithmetic Operator: +,-,*,/,%
 	2. Comparison Operator: (it gives output in true and false / 0 or 1)
				(i)  equality operator: ==, ===, !=, !==
				(ii) Relational Operator: >, <, >=, <=, ==, != 
 	3. Logical Operator: &&, ||, ! (! -> true=false, false=true)
 	4. Assignment Operator: =, +=, -=, *=, /=, %=
 	5. Increment and Decrement Operator: ++, --
 	6. Bitwise Operator: &, |, ^, ~, <<, >>
	7. String Operator: + (can join strings)

#_Switch Case:
 A multi-way decision statement.
 	e.g. = switch(choice)
 		{
   		   case 1: printf("One");
                       break;
    	      	   case 2: printf("Two");
           	   break;
   		   default: printf("Invalid");
 		}

#_Loop:
 	1. for loop ->
 		for(initialization; condition; increment/decrement){}
 	2. While loop ->
 		while(condition){
 			increment/decrement
 			}
 	3. Do while loop ->
 		do{
 		   increment/decrement
 		  }
 		   while(condition);

Difference between for, while and do-while loop : 
=> for : (i) number of iterations is known.
	  (ii) condition is checked before executing the loop body.
	  (iii) the loop may execute zero times.
=> while : (i) number of iterations is known.
	      (ii) condition is checked before executing the loop body.
	      (iii) the loop may execute zero times.
=>do-while : (i) loop must execute at least once.
	          (ii) condition is checked after executing the loop body.
	          (iii) even if the condition is false, the loop executes one time. 

 	Break:    The break statement is used to exit a loop immediately.
 	Continue: The continue statement skips the current iteration** and jumps to the next iteration of the loop.
 	Goto:     goto is a jump statement used to transfer control to a labeled statement in a program.
 		e.g. = int i = 1;
 		        start:
 		        printf("%d ", i);
 		        i++;
 		        if(i <= 3)
    		        goto start;

#_What is Array?
 An array stores multiple values of the same datatype in continuous memory.
 	e.g. = int a[3] = {10, 20, 30}; 
	       int a[2][3] = {
    				      {1, 2, 3},
    				      {4, 5, 6}
			             };

#_What is String? 
 A string is a collection of characters stored in an array.
 		e.g. = char name[ ] = "Hello";
 		1. Character: A character string is an array of characters that	ends with a null character '\0'.
 			e.g. = char str[ ] = "C Programming";  // ends with '\0' automatically
 		2. Pointer: A pointer can point to the first character of a string for easy access and manipulation.
 			e.g. = char *p = "Hello";
 			          printf("%c", *p);  

#_String Handling Functions:
	1. strlen: length of string.
		e.g. = int main(void) {
    			char str[] = "Hello";
			printf("Length: %zu\n", strlen(str));
			return 0;
			}

 	2. strcpy: Copy source to destination.
		e.g. = int main(void) {
    			char src[] = "Hi";
    			char dest[10];
			strcpy(dest, src);
			printf("%s\n", dest);
			return 0;
			}

	3. strcat: Append source to end of destination.
		e.g. = int main(void) {
    			char a[20] = "Hi ";
    			char b[] = "there";
			strcat(a, b);
			printf("%s\n", a);
			return 0;
			}

	4. strcmp: Compare two strings.
		e.g. = int main(void) {
    			char a[ ] = "cat";
    			char b[ ] = "cat";
			if (strcmp(a, b) == 0) {
        			printf("Strings are equal\n");
    			}
    			    return 0;
			} 
	5. fgets(): To read the string
	6. fputs(): To print/write the code
		e.g. = #include <stdio.h>
		     int main() {
    		     	char str[30];
    		       	fgets(str, 30, stdin);   // stdin = standard input -> Keyboard thi input leva									   mate use thay
    		       	fputs(str, stdout);      // stdout = standard output -> Screen par output batava								mate use thay
   		       		return 0;
		      }

#_What is a function?
	A function is a block of code that performs a specific task.
	-> it helps to divide a program into smaller parts, making the program easy to understand, reuse and maintain.
	
	@key points :-
		-a function performs a specific task.
		-it helps in code reusability.
		-it reduces paragraph length.
		-it improves readability.
		-a function can be called multiple times.
	e.g. = int sum (int a, int b)
	       {
			return a+b;
	       }
	     sum(2,3);

	#_Parameters:  variables declared inside the function definition.
	#_Arguments:  actual values or variables you supply when calling the function.
	
	=> Method of argument passing : 
		@ Call by value : when we pass a variable to a function, the function gets a copy, not the original. So, The				        function changes only the copy and the original				        variable stays the same.
			e.g. = #include <stdio.h>
			     void change(int x) {
    				      x = 10;
			       }
			       int main() {
    				   	int a = 5;
    				   	change(a);
    				   	printf("%d", a);
    				   return 0;
			       }

		@ Call by reference : functions cannot directly change a variable, But if we send the address of the variable					     (using pointers), the function can reach and					     modify the original variable.
			e.g. =  #include <stdio.h>
				void change(int *x) {
    				    *x = 10;
				}
				int main() {
    				    int a = 5;
    				    change(&a);
    				    printf("%d", a);
    				   return 0;
				}

#_Recursion:	
A function repeatedly calls itself until a specified stopping condition (base case-it is the condition that stops recursion) is met.
		e.g. = #include <stdio.h>
			void printNumbers(int n) {
    				if(n > 5) return;   // Base case
    				printf("%d ", n);
    				printNumbers(n + 1); // Recursive call
			}
			int main() {
    				printNumbers(1);
    			return 0;
			}

#_Debugging: Debugging is the process of finding and fixing errors (bugs) in a program.

#_Storage classes: 
	storage classes are to control how the variable behaves in memory.

storage classes |  scope  | life time |default value| storage
----------------+---------+-----------+-------------+----------
	  auto      | local - | block -   |   garbage   | stack
				| block   | execution |				|
----------------+---------+-----------+-------------+----------
	register	| local - | block -   |   garbage   | cpu reg
				| block   | execution |				|
----------------+---------+-----------+-------------+----------
	  static	| local - | entire -  |		 0  	| data seg 
	  			| block   |  program  |				|			
----------------+---------+-----------+-------------+----------
	  extern	| global  | entire -  |		 0  	| data seg 
	  			| block   |  program  |				|													

	local-block - a block-scoped variable inside a function
	    auto    - Exist only while function/block runs
	  register  - Exists only while the block/function executes (temporary)
	   static   - Exist throughout the program, keeps its value between function calls
	   extern   - Exist throughout the program, can be accessed in multiple files
	   stack    - Variables exist only while the function runs. (temporary - lifo)
	  cpu reg   - Small, super-fast storage inside the CPU itself and it's used for variables that need fast access.
	  data seg  - data segment Permanent storage while the program runs.
	    heap    - not exactly storage class, but memory area.

#_Preprocessor :
A tool that runs before the actual compilation of a C program.
	-> Works before compiling → prepares the code for the compiler
		e.g. =  #include, #define, #ifdef, #ifndef, #endif

#_Structure : 
It is a user-defined data type that allows you to group different types of variables together under one name.
->Each member gets its own separate memory location. Total size = sum of all members (plus padding). All members can hold valid values simultaneously.
		e.g. = #include <stdio.h>
			 	struct Numbers {
    			     int a;
    			     int b;
				};
			int main() {
    			     struct Numbers n1;
    			     n1.a = 5;
    			     n1.b = 10;
			     	printf("a = %d, b = %d", n1.a, n1.b);
    			   return 0;
			}

#_Union : 
A user-defined data type, just like a structure, but all members share the same memory location.
->All members share the same memory location. Total size = maximum size of the largest member. Only one member is valid at a time.

	e.g. = #include <stdio.h>
		union Data {
    		   int i;
    		   char c;
		};
		int main() {
    		   union Data d;
    		   d.i = 5;    
    		   printf("%d\n", d.i);
    		   d.c = 'A';  
    		   printf("%c\n", d.c);
    		return 0;
		}
	
=> In a structure, each member has its own storage.
=> In a union, all members share the same memory space.

#_Enumeration :
It is a way to give names to a set of numbers.
		e.g. =  #include <stdio.h>
			 	enum Color { Red, Green, Blue };
			 	int main() {
    			   enum Color c;
    			   c = Green;
    			   printf("%d", c);  // prints 1
    			 return 0;
				}

#_File handling :
The process of storing data to a file or reading data from a file using a	program, Useful for storing data permanently (even after the program	ends)
		e.g. = fopen(), fclose(), fprintf() / fscanf(),	fwrite() / fread()
				#include <stdio.h>
				int main() {
    				    FILE *fp;
    				    fp = fopen("data.txt", "a");
    				    if (fp == NULL) {
        			    printf("File error");
        			return 1;
    				}
    				  fprintf(fp, " Students");
    				  fclose(fp);
    				  printf("Data appended successfully");
    				  return 0;
					}

#_Standard libraries :
A collection of pre-written functions and code that you can use in your programs.

	 library |				purpose  
	---------+----------------------------------                
	stdio.h  |input/output(printf, scanf, fopen)
	math.h   |Mathematical functions (sqrt, pow)
	string.h | string handling (strcpy, strlen)
	stdlib.h | General utilities (malloc, free)
 
#_Dynamic memory :
Dynamic Memory is memory that is allocated during program execution (runtime), not in advance.
		e.g. = malloc, calloc, realloc, free	
			=> malloc(n*size) → uninitialized memory / allocate memory at runtime
			=> calloc(n,size) → initialized to 0 / allocate memory and set it to zero
			=> realloc(ptr,new_size) → change the size of allocated memory.
			=> free(ptr) → release memory back to the system.