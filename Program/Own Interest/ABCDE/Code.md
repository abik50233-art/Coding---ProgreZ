#include <stdio.h>

int main()
{
    char arr[]={'A','B','C','D','E'};
    int i,j,n=5;
    for(i=0;i<5;i++)
    {
        j=i;
        while(j!=n)
        {
            printf("%c",arr[j]);
            j++;
        }
        printf("\n");
    }
    for(i=3;i>=0;i--)
    {
        j=i;
        while(j!=n)
        {
            printf("%c",arr[j]);
            j++;
        }
        printf("\n");
    }
    return 0;
}
