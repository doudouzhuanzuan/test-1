#include<stdio.h>

int main()
{
char sentence[100];
int len=0,j,wordlen=0;
gets(sentence);
while(sentence[len]) len++;
for(j=len-1;j>=0;j--)
{
if(sentence[j]>='a'&&sentence[j]<='z'||sentence[j]>='A'&&sentence[j]<='Z')
{
wordlen++;
}
else if(wordlen>0)
{
printf("%*.*s",wordlen,wordlen,&sentence[j+1]);
printf("%c",sentence[j]);
wordlen=0;
}
else
printf("%c",sentence[j]);
}
if(wordlen>0) printf("%*.*s\n",wordlen,wordlen,sentence);
return 0;
}
