# Copystack.c

#include <stdio.h> 
char s[20]; 
int top; 
void init() 
{ 
 top=-1; 
} 
int isempty(){ 
 if(top==-1) 
 return 1; 
 else 
 return 0; 
} 
int isfull() 
{ 
 if(top==19) 
 return 1; 
 else 
 return 0; 
} 
void push(char ch) 
{ 
 if(isfull()==1) 
 printf("stack is full"); 
 else 
 { 
 top++; 
 s[top]=ch; 
 } 
} 
char pop() 
{ 
 char ch; 
 if(isempty()==1) 
 printf("stack is empty"); 
 else 
 { 
 ch=s[top]; 
 top--; 
 } 
 return ch; 
}
 main() 
 { 
 int i,k=0; 
 char temp[20]; 
 init(); 
 char str[20]; 
 printf("enter string "); 
 scanf("%s",str); 
 for(i=0;str[i]!='\0';i++) 
 { 
 push(str[i]); 
 } 
 
 while(!isempty()) 
 { 
 temp[k]=pop(); 
 k++; 
 } 
 
 temp[k]='\0'; 
 
 //Again String push into stack 
 printf("second string :"); 
 for(i=0;temp[i]!='\0';i++) 
 { 
 push(temp[i]); 
 } 
 
 while(!isempty()) 
 { 
 printf("%c",pop()); 
 } 
 } 
