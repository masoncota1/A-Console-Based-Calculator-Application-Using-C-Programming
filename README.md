
****Topic:	Milestone 5: Final Application Release***
______________________________________
Date:	 10 NOV 2021
Revision:	Final
Milestone Summary:	Milestone 5	
______________________________________
In this milestone, students will demonstrate the ability to write complex programs using appropriate and secure use of library functions. 
Students will design and develop the final release of their C programming application. From previous assignments and activities, students should be proficient with the following skills:
++++++++++++++++++++++++++++++++++++++
1.	Writing a C program that performs file I/O
2.	Writing secure code
Execution
Execute this assignment according to the following guidelines:
1.	Update your C application to demonstrate the following features: 
a.	Use of file I/O
b.	Use of secure programming techniques
2.	All code should be fully commented with single-line comments for all logic in code statements and multi-line comments for the all functions as well as code modules.
3.	Complete test cases using the “Test Case Template,” located in the Course Materials that validates all functionality of the program. Positive, negative, and abuse test cases MUST be included in the assignment.
4.	Update the technical design report with the required design documentation.
1.	 		
______________________________________________________________________________
GIT URL:	https://github.com/masoncota1/A-Console-Based-Calculator-Application-Using-C-Programming.git
______________________________________________________________________________
 
 
***Design Documentation***

--Execution**
Execute this assignment according to the following guidelines:
Update your C application to demonstrate the following features: 
____a.	Use of file I/O___

•	This program takes a number from the calculator user and stores in the file program.txt.
•	After you compile and run the program, you can see a text file program.txt created in drive of your computer. When you open the file, you can see the integer you entered. 
•	The fopen( ) function to create a new file or to open an existing file. This call will initialize an object of the type FILE, which contains all the information necessary to control the stream. 
•	The fclose(fptr) function returns zero on success, or fptr if there is an error in closing the file. This function actually flushes any data still pending in the buffer to the file, closes the file, and releases any memory used for the file. The fptr is a constant defined in the header file stdio.h.
•	This program takes a number from the calculator user and stores in the file program.txt.
•	After you compile and run the program, you can see a text file program.txt created in drive of your computer. When you open the file, you can see the integer you entered. 

***Code***

•	/**
•	 * A Console-Based Calculator Application Using C Programming
•	 */
•	
•	#include<stdio.h>
•	#include<conio.h>
•	#include <stdlib.h>
•	int main()
•	{
•	   int num;
•	   FILE *fptr;
•	
•	   // use appropriate location if you are using Windows
•	   fptr = fopen("C:\\program.txt","w");
•	
•	   if(fptr == NULL)
•	   {
•	      printf("Calculator Error!");  
•	      exit(1);            
•	   }
•	
•	   printf("Enter Calculator num: ");
•	   scanf("%d",&num);
•	
•	   fprintf(fptr,"%d",num);
•	   fclose(fptr);
•	}
•	int main()
•	{
•	   float num1, num2, res;
•	   int choice;
•	   do
•	   {
•	      printf("1. Addition\n");
•	      printf("2. Subtraction\n");
•	      printf("3. Multiplication\n");
•	      printf("4. Division\n");
•	      printf("5. Exit\n\n");
•	      printf("Enter Your Choice(1-5): ");
•	      scanf("%d", &choice);
•	      if(choice>=1 && choice<=4)
•	      {
•	         printf("\nEnter any two Numbers: ");
•	         scanf("%f %f", &num1, &num2);
•	      }
•	      switch(choice)
•	      {
•	         case 1:
•	            res = num1+num2;
•	            printf("\nResult = %0.2f", res);
•	            break;
•	         case 2:
•	            res = num1-num2;
•	            printf("\nResult = %0.2f", res);
•	            break;
•	         case 3:
•	            res = num1*num2;
•	            printf("\nResult = %0.2f", res);
•	            break;
•	         case 4:
•	            res = num1/num2;
•	            printf("\nResult = %0.2f", res);
•	            break;
•	         case 5:
•	            return 0;
•	         default:
•	            printf("\nWrong Choice!");
•	            break;
•	      }
•	      printf("\n------------------------\n");
•	   }while(choice!=5);
•	   getch();
•	   return 0;
•	}


5.	All code should be fully commented with single-line comments for all logic in code statements and multi-line comments for the all functions as well as code modules.
 
6.	Update the technical design report with the required design documentation.

Opening a File
You can use the fopen( ) function to create a new file or to open an existing file. This call will initialize an object of the type FILE, which contains all the information necessary to control the stream. The prototype of this function call is as follows −
FILE *fopen( const char * filename, const char * mode );
Closing a File
To close a file, use the fclose( ) function. The prototype of this function is −
int fclose( FILE *fp );
The fclose(-) function returns zero on success, or fptr if there is an error in closing the file. This function actually flushes any data still pending in the buffer to the file, closes the file, and releases any memory used for the file. The fptr is a constant defined in the header file stdio.h.
There are various functions provided by C standard library to read and write a file, character by character, or in the form of a fixed length string.
7.	Complete a screencast, using Loom or a similar free application, that provides the audience with on overview of the project, what functionality was implemented, how your embedded application was designed, and brief functional demonstration of your application running on the embedded board. Make sure to use industry terminology.
 

______________________________________________________________________________________________________________________________________________________________________--
**************************************************************************************************************************************************-********************



# Console-Based-Calculator-Application-Using-C-Programming -
The proposed project is a simple consoled-based computer application in C programing language that performs the basic operations of addition, subtraction, multiplication, and division. 
***Functionality***
calculator application that accepts two input numbers and performs an arithmetic operation such as addition, subtraction, division, and multiplication, then prints the output on the console, so that it can assist me in do mathematics faster. The simple calculator application will have the following operands +, -, *, /, and =. In any situation, the calculator app has to produce a correct result defined by the well-known arithmetic rules. 
After successfully performing the basic operation, the functionality of the calculator need to expand to perform higher functions and warn the user of various errors. If the calculation is impossible the calculator has to display information helping the user resolve the erroneous situation, for example, on encountering division by 0 the output should display “Cannot divide by zero”. 


***Initial Logic Design***


The program is built using C arithmetic operators. The user is presented with a list of choices. Once the user input their choice that operation is performed. The list of operations presented to the user are addition, subtraction, multiplication and division. The C switch statement and C break and continue will be utilized in this application. The program takes an arithmetic operator (+, -, *, /) and two operands from the user. Then it performs the calculation on the two operands depending on the operator entered by the user. Upon entering an operator, the control of programs jumps to respective case matching the operator. The operation takes place and then the break statement end the switch statement. 
Each arithmetic operator performs their respective operation on user inputs and returns the result.
The following are the list of operations to be used in the program
result = a + b; 
result = a - b; 
result = a * b; 
result = a / b; 
  
A flow chat illustrating the logic flow of the main application.

***A flow chat illustrating the logic flow of the main application.***

![image](https://user-images.githubusercontent.com/92959412/138376362-5f640fb9-99b7-4819-8f43-971fb3708c15.png)


 The calculator program needs to show options when run 
“Enter Two Numbers” and 
“Enter your choice” (in regard to operands and should provide a list of operators a follows) Addition (+)
Subtraction (-)
Multiplication (*)
Division (/)
The calculator application demonstrates the following C program features: basic C code structure, the use of standard input and output, use of variables, and the use of loop and decision. Later iterations of the program with higher functionality will utilize the following: the use of data types, the use preprocessor, the modular code by using user defined functions, the use or array or a pointer, and the use of structure and union. 
In the subsequent iterations of the program, the Acceptance Criterion will help in displaying error messages. For example, 
Acceptance Criterion 1: 
Given that and number are presented for an operation; 
And the logic right; 
Then the respective operation is performed. 
Acceptance Criterion 2: 
Given that entered either the numbers are not numeric;
And or the operant is missing; 
Then error message is displayed and operation does not proceed;
Non-functional requirements will be present in addition to the user requirements. While the user story describes the operations that the application must perform, non-functional requirements list the conditions necessary (that are not always documented) to allow the running the program, such as the presence of input and output hardware that must always be powered to facilitate successful running of the desired programs.  


***Link to ScreenCast-O-Matic***

https://screencast-o-matic.com/watch/cr63VJVXWIC#

***Link to Git***

https://github.com/masoncota1/A-Console-Based-Calculator-Application-Using-C-Programming


***Output Screens***
----------------
![Screenshot (2)](https://user-images.githubusercontent.com/92959412/138377790-a81a3e77-7134-482f-9803-bedad9f2ad69.png)
----------------
![Screenshot (3)](https://user-images.githubusercontent.com/92959412/138377810-aa5ad9b3-78c0-4610-85d0-3aecd4824eb1.png)
----------------
![Screenshot (5)](https://user-images.githubusercontent.com/92959412/138377834-25eb0e97-63ac-4c7b-932a-edb2f3679920.png)

---------------

![Screenshot (6)](https://user-images.githubusercontent.com/92959412/138377749-6b73e2b5-42a2-479f-9652-157ea203d3fe.png)
---------------



