#include <stdio.h>
int n,i,j,c;
int main()
{
    do
    {
        printf("Enntrer l'ordre de la matrice:");
        scanf("%d",&n);
    } while(n<2);

    int a[n][n];

    for (i=0; i<n; i++)
    {
        for (j=0;j<n;j++)
        {
            printf("Entrer l'element d'indice (%d-%d)",i,j);
            scanf("%d", &a[i][j]);
        }
    }
        for(i=0; i<n; i++)
    {
        for(j=0; j<n; j++)
        {
            if (i==j)
            {
                c=a[i][j];
                a[i][j]=a[i][n-1-i];
                a[i][n-1-i]=c;
            }
        }

    }
      for(i=0; i<n; i++) 
    {
      for(j=0; j<n; j++)
            {
                printf("Entrer l'element d'indice (%d-%d) est: %d\n",i,j,a[i][j]);
            }
    }
    return 0;
}
