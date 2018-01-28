# hello-world
#include <stdio.h>
char newstr[80];
void main()
{
	char str[80],c_begin,c_end;
	char *fun(char *p,char c_begin,char c_end);

	scanf("%s",str);
	getchar();
	c_begin=getchar();
	getchar();
	c_end=getchar();
	puts(fun(str,c_begin,c_end));
}
char *fun(char *str,char c_begin,char c_end)
{
	int i,j;
	static char st[80];
	for(i=0;i<80;i++)
	{
		if(c_begin==str[i])break;
	}
	for(j=i;j<80;j++)
	{
		st[j-i]=str[j];
		if(str[j]==c_end)break;
	}
	st[j-i+1]='\0';
	return st;
}
