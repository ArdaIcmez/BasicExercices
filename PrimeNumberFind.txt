#include <stdio.h>

int main(void) {
	unsigned i = 7;
	unsigned j=1;
	unsigned int a=2;
	unsigned int k;
	int isTrue=1;
	int primemat[10000]={ 0 };
	primemat[0]=5;
	for(i=7;j!=9999;i+=a)
	{
		isTrue=1;
		for(k=0;k<j;k++)
		{
			if(!(i%primemat[k]))
			{
				isTrue=0;
				break;
			}
		}
		if(isTrue)
		{
			primemat[j]=i;
			j++;
		}
		a=6-a;
	}
			printf("%d is : %d\n",j,primemat[j-1]);
	return 0;
}