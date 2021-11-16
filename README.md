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
We use printf() function with %d format specifier to display the value of an integer variable (veselais skaitlis).
Similarly %c is used to display character (simbols), %f for float variable (realais skaitlis), %s for string variable, %lf for double and %x for hexadecimal variable.

To generate a newline,we use “\n” in C printf() statement. jauna rinda.



DATU TIPI
char: The most basic data type in C. It stores a single character and requires a single byte of memory in almost all compilers.
int: As the name suggests, an int variable is used to store an integer.
float: It is used to store decimal numbers (numbers with floating point value) with single precision.
double: It is used to store decimal numbers (numbers with floating point value) with double precision. 


A format specifier for scanf follows this prototype:

%[*][width][length]specifier


Знак *, помещенный после % и перед спецификатором формата, считывает данные указанного типа, но подавляет их присваивание. Таким образом, код

scanf ("%d%*c%d", &х, &у);

при вводе последовательности 10/20 присваивает значение 10 переменной х, отбрасывает символ / и присваивает значение 20 переменной у.














//homework called dec2bin

#include <stdio.h>

#include <math.h>

long long convert(int);

int main() {

char n;

long long int bin;//what is char??? it is data type

printf("Cienījamais lietotāj, lūdzu ievadi skaitli: ");//shows this text

scanf("%d", &n);

printf("Tu ievadījis skaitli: %c\n", n);

bin = convert(n);

printf("Decimals %c ir binarais  %lld ",n, bin);

return 0;

}

long long convert(int n) {

long long  int bin = 0;

int rem, i = 1;

while (n!=0) {

rem = n % 2;//ostatok

n /= 2;//rezultat delenia

bin += rem * i;//bin + ostaok * i

i *= 10;//prisvaivanie znachenija umnozennoe na 10

}

return bin;

}














nodarbiba 06 konspekts

GNU nano 4.8                     homework002.c                      Изменён  

//datu tipi - wikipedia vai c tehniska secifikacija

#include<stdio.h>

int main()

{

char c1; //char datu tipa mainiga deklaresana

//turpmak koda var tikt izmantots identifikators "c1"

//griezoties pie c1, mes griezisimies pie noteikta 1 baita

//liela atminas apgabala

//pec deklaresanas atminas apgabala aizpildijums nav zinams

//0101 1110 vai 0111 0000 vai 0000 1010

printf("Statisks teksts - mainiga c1 vertiba pec deklaresanas - %d\n",c1);

char c2 = 100; // char datu tipa mainiga definesana

printf("Statisks teksts - mainiga c2 vertiba pec deklaresanas - %d\n",c2);

//mainiga identifikatora piemers - var_count, Var_count, var_count

//mainigo nosaukumos nedrikst izmantot atstarpes, domu zimes utt.

c2 = 65;

// atbilstosi char b(info par zimi 0+ un 1-) bbb bbbb

//65 = 64 + 1 = 1*2^6+1*2^0 =  0100 0001 (viens pie 0tas un 6tas pakapes)

// tas ir 42 (hex) un 101 (oct) 

printf(" mainiga c2 vertiba pec jaunas pieskirsanas - %d (dec)\n",c2);

printf(" mainiga c2 vertiba pec jaunas pieskirsanas - %x (hex)\n",c2);

printf(" mainiga c2 vertiba pec jaunas pieskirsanas - %o (oct)\n",c2);

printf(" mainiga c2 vertiba pec jaunas pieskirsanas - %c (simbols)\n",c2);

//%c ir simbols

c2 = 0x42;

printf("Mainīgā c2 vērtība pēc jaunas vērtības piešķiršanas:\n");

printf("kā dec - %d, kā hex - %x, kā oct - %o, kā simbols - %c\n",c2,c2,c2,c2);

c2 = 'K';

printf("\nMainīgā c2 vērtība pēc jaunas vērtības piešķiršanas:\n");

printf("kā dec - %d, kā hex - %x, kā oct - %o, kā simbols - %c\n",c2,c2,c2,c2);

c2 = 1000;

printf("\nMainīgā c2 vērtība pēc jaunas vērtības piešķiršanas:\n");

printf("kā dec - %d, kā hex - %x, kā oct - %o, kā simbols - %c\n",c2,c2,c2,c2);

//1000 = 512  + 256  + 128 + 64  + 32  +  8 =
//       1*2^9+1*2^8 +1*2^7+1*2^6+1*2^5+1*2^3
//        0000 0011  1110 1000
//                   1|110 1000
//                   -|001 0111
//atbilstoši char b|bbb       1
//65 = 64 + 1 = 1*2^6 + 1-|001 1000 => -(1*2^3 + 1*2^4) = -(24) = -24

return 0;

}











Nodarbība 16.11
#include<stdio.h>
#define N 100
 
int main()
{
char sentence[N];
FILE * pFile;
 
pFile = fopen("text.txt","r");
if(pFile != NULL)
 {
 while( fscanf(pFile,"%[^\n]\ns",sentence) != EOF )
  {
  printf("%s\n",sentence);
  }
 fclose(pFile);
 }
 
return 0;
}



fwrite:
#include<stdio.h>
#define N 100
 
int main()
{
int a = 10000;
FILE * pFileTXT;
FILE * pFileBIN;
 
pFileTXT = fopen("test.txt","w");
if(pFileTXT != NULL)
 {
 fprintf(pFileTXT,"%d",a);
 fclose(pFileTXT);
 }
 
pFileBIN = fopen("test.bin","wb");
if(pFileBIN != NULL)
 {
 fwrite(&a, sizeof(int), sizeof(a)/sizeof(int), pFileBIN);
 fclose(pFileBIN);
 }
 
return 0;
}






fread:
#include<stdio.h>
#define N 100
 
int main()
{
int a;
FILE * pFileBIN;
 
pFileBIN = fopen("test.bin","rb");
if(pFileBIN != NULL)
 {
 fread(&a, sizeof(int), sizeof(a)/sizeof(int), pFileBIN);
 fclose(pFileBIN);
 }
 
 printf("%d\n",a);
 
return 0;
}

 
 
 
 
 
 
 Cīņas rezultāts
 
 /* fread example: read an entire file */
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main () {
  FILE * pFile;
  long lSize;
  unsigned char * buffer;
  size_t result;
  char a;

  pFile = fopen ( "test.c" , "rb" );
  if (pFile==NULL) {fputs ("File error",stderr); exit (1);}

  // obtain file size:
  fseek (pFile , 0 , SEEK_END);
  lSize = ftell (pFile);
  printf("test.c faila izmērs baitos: %ld\n",lSize);
  rewind (pFile);

  // allocate memory to contain the whole file:
  buffer = (char*) malloc (sizeof(char)*lSize + 1);
  if (buffer == NULL) {fputs ("Memory error",stderr); exit (2);}

  //printf("buffer izmērs baitos: %ld\n",sizeof(buffer));
  printf("piešķiramais izmērs baitos: %ld\n",sizeof(char)*lSize+1);
  printf("strlen(buffer) rezultāts pirms dati ir nolasīti: %ld\n",strlen(buffer));
  printf("%s",buffer);
  printf("\n");

/*
  for(int i=0;i<lSize+5;i++)
    printf("%d %c %d\n",i,buffer[i],buffer[i]);
  printf("\n");
*/

  // copy the file into the buffer:
  result = fread (buffer,sizeof(char),lSize,pFile);
  if (result != lSize) {fputs ("Reading error",stderr); exit (3);}
  buffer[lSize]='\0';

  /* the whole file is now loaded in the memory buffer. */
  printf("strlen(buffer) rezultāts pēc dati ir nolasīti: %ld\n",strlen(buffer));
  printf("%s",buffer);
  printf("\n");

/*
  for(int i=0;i<lSize;i++)
    printf("%d %c %d\n",i,buffer[i],buffer[i]);
  printf("\n");
*/

  // terminate
  fclose (pFile);
  free (buffer);
  fflush(stdout);
  scanf("%c",&a);
  return 0;
}
 
 

