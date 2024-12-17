(CN)  character stuffing
#include<stdio.h> 
#include<stdlib.h> 
int main() 
{ 
char c[50],d[50],t[50]; 
int i,m,j,ch; 
do 
{ 
  printf("\n Enter the Choice 1.Stuff 2.Destuff 3.Exit :--"); 
  scanf("%d",&ch); 
    switch(ch) 
    { 
    case 1: 
    printf("Enter the Number of Characters\n"); 
scanf("%d",&m); 
printf("\n Enter the Original Data \n"); 
for(i=0;i<m+1;i++) 
{ 
scanf("%c",&c[i]); 
} 
d[0]='D'; 
d[1]='L'; 
d[2]='E'; 
d[3]='S'; 
d[4]='T'; 
d[5]='X'; 
for(i=0,j=6;i<m+1;i++,j++) 
{ 
if((c[i]=='d'&&c[i+1]=='l'&& c[i+2]=='e')) 
{ 
d[j]='D'; 
j++; 
d[j]='L'; 
j++; 
d[j]='E'; 
j++; 
m=m+3; 
} 
d[j]=c[i]; 
} 
m=m+6; 
m++; 
d[m]='D'; 
m++; 
d[m]='L'; 
m++; 
d[m]='E'; 
m++; 
 
 
d[m]='E'; 
m++; 
d[m]='T'; 
m++; 
d[m]='X'; 
m++; 
printf("\n Transmitted Data: \n"); 
for(i=0;i<m;i++) 
{ 
printf("%c",d[i]); 
} 
break; 
case 2: 
for(i=6,j=0;i<m-6;i++,j++) 
{ 
if(d[i]=='D'&&d[i+1]=='L'&&d[i+2]=='E'&&d[i+3]=='d'&&d[i+4]=='l'&&d[i+5]=='e') 
i=i+3; 
t[j]=d[i]; 
} 
printf("\n\n Received data:"); 
for(i=0;i<j;i++) 
{printf("%c",t[i]); 
} 
break; 
case 3: 
exit(0); 
break; 
} 
} 
while(ch<4); 
return 0; 
}
