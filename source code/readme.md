#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int header()
{
printf("\n \t \t \t*************************************************************\n");
printf("\n \t \t \t \t \t        |:-WELCOME TO:-|\n");
printf("\n \t \t \t \t\t   |:-  L&T BOOK STORE :-  |\n");
printf("\n \t \t \t \t        |:-   NH-75, , BANGALORE:-  |\n");
printf("\n \t \t \t*************************************************************\n");
}
struct list
{
char author[20];
char title[30];
float price;
struct
{
char month[10];
int year;
}date;
char publisher[10];
int quantity;
};
//to search the book in the list
int search(struct list table[],char c1[],char c2[],int n);
//to get the input string
int get(char string[]);
main()
{
int index,no_of_record;
char title[30],author[20];
char responce[10],quantity[10];
struct list book[]=
{
{
"Ritche","C Language",245.00,"May",1977,"PHI",15
},
{
"Yashwant Kanetkar","Let us c",550.00,"Jan",2001,"OUP",20
},
{
"Balagurusamy", "Beginning", 527.50,"Nov",2012,"WILEY",15
},
{
"R K Jain","Engineering Mathematics",225.00,"Oct",2010,"TMH",10
},
{
"Kochan","Programming in C",275.50,"july",1983,"hayden",25
},
{
"Rajiv Mall", "Software Engineering",310.00,"Jun",2011,"TMH",
},
{
"Balagurusamy","Basic",268.00,"Jan",1984,"TMH",20
},
{
"B S Grewal", "Advanced Eng. Mathematics",420.00,"Aug",2009,"TMH",15
},
{
"Balagurusamy","COBOL",260.00,"Dec",1988,"Macmillan",25
},
{
"Godbole & Kahate","Web Technologies",340.00,"Sep",2012,"TMH",20
}
};
 //calculate how many book in our list
no_of_record=sizeof(book)/sizeof(struct list);
do
{
header();
printf("\n\n\n\n\t:- ENTER THE TITLE AND AUTHOR OF THE BOOK WHICH YOU WANT TO PURCHASE :- \n");
printf("\n\n\t:- TITLE :-");
get(title);
printf("\n\n\t:- AUTHOR :-");
get(author);
index=search(book, title, author, no_of_record);
if(index !=-1)
{
printf("\n\n YOUR DESIRE BOOK AVAILBLE IN THE STOCK.\n\n");
printf("	[AUTHOR], 			[TITLE],				[Price],([Month][Year]), [Publisher]\n");
printf("-------------------------------------------------------------");
printf("\n	%s, 			%s,			%.2f, (%s-%d), %s \n\n",book[index].author,book[index].title,book[index].price,book[index].date.month,book[index] .date.year,book[index].publisher);
printf("\n\n ENTER THE NUMBER OF COPIES:");
get(quantity);
no_of_record=atoi(quantity);
if(atoi(quantity)<=book[index].quantity)
printf("\n\nCOST OF THE %d COPIES IS=%.2f\n ",atoi(quantity),book[index].price*atoi(quantity));
else
printf("\n REQUIRED COPIES NOT IN THE STOCK \n\n");
}
else
printf("\n YOUR DESIRED BOOK IS NOT IN THE STOCK.\n\n");
printf("\n DO YOU WANT TO PURCHASE ANY OTHER BOOK ? (Y/N):");
get(responce);
}
while(responce[0]=='y'||responce[0]=='y');
printf("\n\n THANK YOU....!!!!\n");
printf("Designed By: Abdullah\n");
printf("SFID:-265148\n\n\n");
}
int get(char string[])
{
char c;
int i=0;
do
{
c=getchar();
string[i++]=c;
}
while(c !='\n');
string[i-1]='\0';
}
int search(struct list table[],char c1[],char c2[],int n)
{
int i;
for(i=0;i<n;i++)
if(strcmp(c1,table[i].title)==0 && strcmp(c2,table[i].author)==0)
return(i);
return(-1);
}
