# RTR-105 
Datormācība (pamatkurss) elektroniskā klade

CLI Command-line interface (processes commands to a computer program in the form of lines of text)
GUI graphical user interface
md - Markdown (is a lightweight markup language for creating formatted text using a plain-text editor)

whoami It is a concatenation of the words "Who am I?" and prints the effective username of the current user when invoked
   who command lets you display the users currently logged in to your Linux operating system.
   pwd command stands for print working directory. It is one of the most basic and frequently used commands in Linux (Where am i?)
   ls command is used to list files or directories in Linux and other Unix-based operating systems. Just like you navigate in your File explorer or Finder with a GUI, the ls command allows you to list all files or directories in the current directory by default, and further interact with them via the command line.
man ls - info about ls

ls:
-l  use a long listing format
-a do not ignore entries starting with .
-A do not list implied . and ...
'ls -a -l' un 'ls -l -a' un 'ls -la' same
ls -lt большой список



cd means open catalog
cd .. one step back

mkdir - make a folder
> means create a file
rm means remove/delete

echo to write text
echo "text" < "file name"
text goes to file

cat - to read text from file in terminal

gcc is compilator (example: gcc dialogs.c -o dialogs.out)
./ open program

 tree is a recursive directory listing command or program that produces a depth-indented listing of files

(/home/pl/test.txt. Второй путь указывает, что в корневом каталоге есть папка home, в ней находится каталог pl, в котором имеется файл test.txt.)

PROGRAM 1:

#include<stdio.h>

int main ()

{

long long i,g;

printf("Cienījamais lietotāj, lūdzu ievadi skaitli: ");

fflush(stdout);

scanf("%ld", &i);

printf("Tu ievadījis skaitli: %ld\n", i);

fflush(stdout);

printf("Cienījamais lietotāj, lūdzu ievadi otro skaitli: ");

fflush(stdout);

scanf("%ld", &g);

printf("Tu ievadījis skaitli: %ld\n", g);

fflush(stdout);

long long x=i*g;

printf("Reizināšanas rezultāts ir: %ld\n ", x);

return 0;

}

Specifikatori
![image](https://user-images.githubusercontent.com/47148502/137630405-f0143093-0d59-4dab-9ca7-de1a35586294.png)


%s - Take the next argument and print it as a string
%d - Take the next argument and print it as an int
In C, & is called the address operator. The expression &i means, "The memory address of the variable i."

In C programming language, printf() function is used to print the (“character, string, float, integer, octal and hexadecimal values”) onto the output screen.
We use printf() function with %d format specifier to display the value of an integer variable.
Similarly %c is used to display character, %f for float variable (realais skaitlis), %s for string variable, %lf for double and %x for hexadecimal variable.
To generate a newline,we use “\n” in C printf() statement.



DATU TIPI
char: The most basic data type in C. It stores a single character and requires a single byte of memory in almost all compilers.
int: As the name suggests, an int variable is used to store an integer.
float: It is used to store decimal numbers (numbers with floating point value) with single precision.
double: It is used to store decimal numbers (numbers with floating point value) with double precision. 
