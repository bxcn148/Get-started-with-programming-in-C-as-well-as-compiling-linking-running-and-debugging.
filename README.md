Download link :https://programming.engineering/product/get-started-with-programming-in-c-as-well-as-compiling-linking-running-and-debugging/


# Get-started-with-programming-in-C-as-well-as-compiling-linking-running-and-debugging.
Get started with programming in C, as well as compiling, linking, running, and debugging.
Introduction

This assignment is a quick assignment to get you started with programming in C, as well as compiling, linking, running, and debugging. Your task is to write 5 small C programs. Your program must follow the input-output guidelines listed in each section exactly, with no additional or missing output.

No cheating or copying will be tolerated in this class. Your assignments will be automatically checked with plagiarism detection tools that are pretty powerful. Hence, you should not look at your friend’s code. See CS department’s academic integrity policy at: http://academicintegrity.rutgers.edu/

First: Prime Numbers (5 Points)

You have to write a program that will read an array from a le and print if the numbers in the le are right truncatable primes. A right truncatable prime is a prime number, where if you truncate any numbers from the right, the resulting number is still prime. For example, 3797 is a truncatable prime number number because 3797, 379, 37, and 3 are all primes.

Input-Output format: Your program will take the le name as input. The rst line in the le provides the total number of values in the array. The subsequent lines will contain an integer value. For example a sample input le \ le1.txt” is:

3

397

73

47

Your output will contain the same number of lines as the number of lines in the input le. Each line will either say yes if the corresponding integer is a truncatable prime or no if the corresponding integer is not a truncatable prime.


$./first file1.txt

no

yes

no

We will not give you improperly formatted les. You can assume that the les exist and all the input les are in proper format as above.

Second: Ordered Linked List (10 points)

In this part, you have to implement a linked list that maintains a list of integers in sorted order. For example, if a list already contains 2, 5 and 8, then 1 will be inserted at the start of the list, 3 will be inserted between 2 and 5 and 10 will be inserted at the end.

Input format: This program takes a le name as an argument from the command line. The le contains successive lines of input. Each line contains a string, either INSERT or DELETE, followed by a space and then an integer. For each of the lines that starts with INSERT, your program should insert that number in the linked list in sorted order if it is not already there. Your program should not insert any duplicate values. If the line starts with a DELETE, your program should delete the value if it is present in the linked list. Your program should silently ignore the line if the requested value is not present in the linked list. After every INSERT and DELETE, your program should print the content of the linked list. The values should be printed in a single line separated by a single space. There should be no leading or trailing white spaces in each line of the output. You should print EMPTY if the linked list is empty.

Output format: At the end of the execution, your program should have printed the content of the linked list after each INSERT or DELETE operation. Each time the content is printed, the values should be on a single line separated by a single space. There should be no leading or trailing white spaces in each line of the output.You should print EMPTY if the linked list is empty. Your program should print \error” (and nothing else) if the le does not exist. You can assume that there will be at least one INSERT or DELETE in each le.


Example Execution:

Lets assume we have 2 text les with the following contents:

file1.txt:

INSERT 1

INSERT 2

DELETE 1

INSERT 3

INSERT 4

DELETE 4

INSERT 5

DELETE 5

file2.txt:

INSERT 1

DELETE 1

INSERT 2

DELETE 2

INSERT 3

DELETE 3

INSERT 4

DELETE 4

INSERT 5

DELETE 5

Then the result will be:

$./second file1.txt

1

2

2

2 3

2 3 4

2 3

2 3 5

2 3

$./first file2.txt


EMPTY 2 EMPTY 3 EMPTY 4 EMPTY 5 EMPTY


$./second file3.txt

error

Third: Stack and Queue (10 points)

In this part of the assignment, you will implement a linked list that supports both stack and queue.

The idea is to have a single linked list that supports three operations:

ENQUEUE: Queues a value at the end of the linked list

PUSH: Pushes a value at the beginning of the linked list

POP: Pops and removes the value at the beginning of the linked list.

Input format: This program takes a le name as an argument from the command line. The le contains successive lines of input. Each line contains a string, either ENQUEUE or PUSH followed by a space and then an integer OR just the word POP without anything following it. For each line that starts with ENQUEUE, your program should insert that number at the end of the linked list (like a queue). If the line starts with a PUSH, your program should insert that number at the beginning of the linked list (like a stack). If the line says POP, your program should pop and delete the rst value at the beginning of the linked list.

After every ENQUEUE, PUSH, and POP, your program should print the content of the linked list. The values should be printed in a single line separated by a single space. There should be no leading or trailing white spaces in each line of the output. You should print EMPTY if the linked list is empty.

Output format: At the end of the execution, your program should have printed the content of the linked list after each ENQUEUE, PUSH, or POP operation. Each time the content is printed, the values should be on a single line separated by a single space. There should be no leading or trailing white spaces in each line of the output.You should print EMPTY if the linked list is empty. Your program should print \error” (and nothing else) if the le does not exist. You can assume that there will be at least one ENQUEUE, PUSH, or POP operation in each le.

Example Execution:

Assume we have a text le with the following contents:

file.txt:

PUSH 1

ENQUEUE 2

PUSH 3

PUSH 4

POP

ENQUEUE 5

POP

POP

POP

POP


The the results will be:

$./third file.txt

1

2

3 1 2

4312

3 1 2

3125

2 5

2 5

5 EMPTY

Fourth: Magic Square (10 Points)

A magic square is an arrangement of the numbers from 1 to n2 in an (n x n) matrix, with each number occurring exactly once, and such that the sum of the entries of any row, any column, or any main diagonal is the same.

An example of a Magic Square is as such:

8 1 6

3 5 7

4 9 2

In this case, the sum of all entries in a given row, column or main diagonal is equal to 15.

In this part, you will create a program that automatically creates a magic square for an odd-ordered matrix, i.e. n n matrix where n is an odd number. There is a famous method for creating magic squares for matrix of odd order: https://en.wikipedia.org/wiki/Magic_square#A_method_ for_constructing_a_magic_square_of_odd_order

Method: This method is applicable for all odd-ordered matrix. We illustrate the method by creating a 3 3 magic square.

The rst step starts with a number 1 at the center column of the rst row: 1

After that, we ll incrementally larger number to the cell diagonally up and right, one at a time. If the new cell goes outside of the matrix, we wrap around to the other side. For example, since there is no cell above and to the right of our 1, we ll the bottom right cell with a 2. It can


also be considered that the sides of the matrices are connected to the opposite side when traversing the cells.


error

Fifth: Matrix Determinant(15 points)

In linear algebra, the determinant is a value that can be computed with a square matrix. The determinant describes some properties about the square matrix. Determinants are used for solving linear equations, computing inverses, etc, and is an important concept in linear algebra. In the fth part of the assignment, you will write a program that computes the determinant of any n n matrix. You will have to carefully manage malloc and free instructions to successfully compute the determinants.

Determinant

Given a square n n matrix M, we will symbolize the determinant of M as Det(M). You can compute Det(M) as follows:

1 1 matrix The determinant of the 1 1 matrix is the value of the element itself. For example,

Det( 3 ) = 3

2 2 matrix The determinant of a 2 2 matrix can be computed using the following formula:

Det(

a

b

) = ad bc

c

d

For example,

3

4

)=1 4

2 3=4

6 = 2

Det(

1

2

3 3 matrix The determinant of a 3 3 matrix can be computed modularly. First, let’s de ne a 3 3 matrix:

3

a b c

M = 4

d

e

f

5

g

h

i

The formula for computing the determinant of M is as follows:

Det(M) = a Det(Ma) b Det(Mb) + c Det(Mc)

The matrix Ma is a 2 2 matrix that can be obtained by eliminating the row and column that a belongs to in M. More speci cally, since a is on the rst row and rst column, we eliminate the rst row and rst column from M:

3

a b c

4d e f5

g h i

This gives us a 2 2 matrix for Ma:

Ma =

e

f

h

i

Mb can be computed similarly. Since b is on the rst row and second column, we eliminate the rst

row and second column from M:

3

2a

b

c

4

d

e

f

5

g

h

i

This gives us a 2 2 matrix for Mb:

g

i

Mb =

d

f

Mc can be computed by removing the rst row and the third column from M since c is on the rst row and third column. Thus,

2a

b

c

3

d

e

f

5

4g

h

i

Mc =

g

h

d

e

Finally, the formula for computing the determinant of M is:

Det(M) = a Det(

h

i

)

b Det(

g

i

) + c Det(

g

h

)

e

f

d

f

d

e

For example, we can compute the determinant of the following matrix,

22

7

63

9

5

1

M=44

3

85

as follows:

)

7 Det(

) + 6 Det(

) = 2(37) 7(68) + 6(7) = 360

Det(M) = 2 Det(

3

8

4

8

4

3

5

1

9

1

9

5

n n matrix Computing the determinant of an n n matrix can be considered as a scaled version of computing the determinant of a 3 3 matrix. First, let’s say we’re given an n n matrix,

2x2;1

x2;2

x2;3

: : : x2;n3

6

x1;1

x1;2

x1;3

: : : x1;n

7

M =

x3.;1 x3.;2 x3.;3 : : : x3.;n

6

..

..

..

..

7

6

7

6x

x

x

: : : x

7

4

5

6

n;1

n;2

n;3

n;n

7

In essence, we have to pivot each element in the rst row and create (n 1) (n 1) matrix for each pivot element (in the case of computing the determinant of 3 3 matrix, we had Ma that corresponds to a, etc).

For example, when we pivot x1;1, we create the corresponding (n

1) (n

1) matrix for x1;1 by

deleting the 1st row and 1st column:

: : : x2;n3

x2;2

x2;3

: : : x2;n

2x2;1

x2;2

x2;3

x1;1

x1;2

x1;3

: : : x1;n

2

3;2

3;3

: : :

3;n3

x

x

x

: : : x

6

7

6

x

x

x

7

M1;1 =

3.;1

3.;2

3.;3

3.;n

=

...

...

...

6

..

..

..

..

7

x

x

: : :

x

6

x

x

x

: : : x

7

6

n;2

n;3

n;n

7

6

n;1

7

6

7

6

n;2

n;3

n;n

7

4

5

4

5

Similarly, we can create M1;2, M1;3, : : : by pivoting x1;2, x1;3, and so on:

x2;n

2x2;1

x2;2

x2;3

: : : x2;n3

x2;1

x2;3

:: :: ::

x1;1

x1;2

x1;3

: : : x1;n

2

3;1

3;3

3;n3

x

x

x

: : : x

6

7

6

x

x

x

7

M1;2 =

3.;1

3.;2

3.;3

3.;n

=

...

...

...

6

..

..

..

..

7

x

x

: : :

x

6

x

x

x

: : : x

7

6

n;1

n;3

n;n

7

6

n;1

7

6

7

6

n;2

n;3

n;n

7

4

5

4

5

2x2;1

x2;2

x2;3

: : : x2;n3

x2;1

x2;2

x2;4

: : : x2;n

x1;1

x1;2

x1;3

: : : x1;n

2

3;1

x

3;2

3;4

: : :

3;n3

x

x

x

: : : x

M1;3 = 6

7 =

x

x

x

7

3.;1

3.;2

3.;3

3.;n

...

...

...

...

6

..

..

..

..

7 6

x

x

x

: : : x

6

x

x

x

: : :

x

7 6

n;1

n;2

n;4

n;n

7

6

n;1

7

6

7

6

n;2

n;3

n;n

7

4

5

4

5

Finally, you can compute the determinant of M using the following formula:

Det(M) = x1;1 Det(M1;1) x1;2 Det(M1;2)+x1;3 Det(M1;3) x1;4 Det(M1;4)+x1;5 Det(M1;5) : : :

The above formula can be shortened to the following formula:

Det(M) = ni=1( 1)i 1x1;i Det(M1;i)

This general formula for computing the determinant of n n matrix applies to all n. The formula for computing the determinant of 2 2 and 3 3 matrix is exactly the same as this formula.

Input-Output format:

Your program should accept a le as command line input. The format of a sample le test3.txt is shown below:

3

2

7

6

9

5

1

4

3

8

The rst number (3) corresponds to the size of the square matrix (n). The dimensions of the matrix will be n x n. You can assume that n will not be greater than 20. The rest of the le contains the content of the matrix. Each line contains a row of the matrix, where each element is separated by a tab. You can assume that there will be no malformed input and the matrices will always contain valid integers.

Your program should output the determinant of the n n matrix provided by the le.


Example Execution

A sample execution with above input le test3.txt is shown below:

$./fifth test3.txt

-360

Structure of your submission folder

All les must be included in the pa1 folder. The pa1 directory in your tar le must contain 5 subdirectories, one each for each of the parts. The name of the directories should be named rst through fth (in lower case). Each directory should contain a c source le, a header le (if you use it) and a Make le. For example, the subdirectory rst will contain, rst.c, rst.h (if you create one) and Make le (the names are case sensitive).

pa1

|- first

|– first.c

|– first.h (if used)

|– Makefile

|- second

|– second.c

|– second.h (if used)

|– Makefile

|- third

|– third.c

|– third.h (if used)

|– Makefile

|- fourth

|– fourth.c

|– fourth.h (if used)

|– Makefile

|- fifth

|– fifth.c

|– fifth.h (if used)

|– Makefile

Submission

You have to e-submit the assignment using Canvas. Your submission should be a tar le named pa1.tar. To create this le, put everything that you are submitting into a directory (folder) named pa1. Then, cd into the directory containing pa1 (that is, pa1’s parent directory) and run the following command:

tar cvf pa1.tar pa1

To check that you have correctly created the tar le, you should copy it (pa1.tar) into an empty directory and run the following command:


tar xvf pa1.tar

This should create a directory named pa1 in the (previously) empty directory.

The pa1 directory in your tar le must contain 5 subdirectories, one each for each of the parts. The name of the directories should be named rst through fth (in lower case). Each directory should contain a c source le, a header le and a make le. For example, the subdirectory rst will contain, rst.c, rst.h and Make le (the names are case sensitive).

AutoGrader

We provide a custom autograder to test your assignment. The custom autograder is provided as pa1 autograder.tar. Executing the following command will create the autograder folder.

$tar xvf pa1_autograder.tar

There are two modes available for testing your assignment with the custom autograder

First mode

Testing when you are writing code with a pa1 folder

Lets say you have a pa1 folder with the directory structure as described in the assignment.

Copy the folder to the directory of the autograder (i.e., pa1 autograder)

Run the custom autograder with the following command

$python auto grader.py

It will run your programs and print your scores.

Second mode

This mode is to test your nal submission (i.e, pa1.tar)

Copy pa1.tar to the pa1 autograder directory

Run the autograder with pa1.tar as the argument. The command line is

$python auto grader.py pa1.tar

Scoring

The autograder will print out information about the compilation and the testing process. At the end, if your assignment is completely correct, the score will something similar to what is given below.

You scored

5.0 in second


5.0 in fourth

5.0 in third

7.5 in fifth

2.5 in first

Your TOTAL SCORE = 25.0 /25

Your assignment will be graded for another 25 points with test cases not given to you

Grading Guidelines

This is a large class so that necessarily the most signi cant part of your grade will be based on programmatic checking of your program. That is, we will build the binary using the Make le and source code that you submitted, and then test the binary for correct functionality against a set of inputs. Thus:

You should not see or use your friend’s code either partially or fully. We will run state of the art plagiarism detectors. We will report everything caught by the tool to O ce of Student Conduct.

You should make sure that we can build your program by just running make.

Your compilation command with gcc should include the following ags: -Wall -Werror -fsanitize=address

You should test your code as thoroughly as you can. For example, programs should not crash with memory errors.

Your program should produce the output following the example format shown in previous sections. Any variation in the output format can result in up to 100% penalty. Be especially careful to not add extra whitespace or newlines. That means you will probably not get any credit if you forgot to comment out some debugging message.

Your folder names in the path should have not have any spaces. Autograder will not work if any of the folder names have spaces.

Be careful to follow all instructions. If something doesn’t seem right, ask on discussion forum.
