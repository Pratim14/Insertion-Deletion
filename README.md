# Insertion-Delet

#include <stdio.h>

void disp();
void insert();
void del();
int i,n;
int arr[100];

int main()
{
    int ch;
    char c;
    int i,arr[100];
    printf("\n Enter the size of Array\n ");
    scanf("%d",&n);

    printf("\n ***********Enter the array elements************ \n ");
    for(i=0;i<n;i++)
    {
        printf(" \n arr[%d] :: ",i);
        scanf("%d",&arr[i]);
    }
 
   printf(" \n Enter 1-> Insert 2-> Delete 3->Display\n ");
    scanf("%d",&ch);
    do
    {
    switch(ch)
    {
        case 1:
            insert(arr);
            disp(arr);
            break;

        case 2:
            del(arr);
            disp(arr);
            break;

        default:
            printf("\n Invalid input\n");
    }
    printf(" \n Enter y/n to continue");
    scanf("%c",&c);

    }
    while(c!=n);

}

      void insert(int arr[])
      {
        int v,p;
        printf("\n Enter the value and position of the element to be inserted \n");
        scanf("%d%d",&v,&p);

            for (i=n-1;i>=p-1;i--)
                arr[i+1]=arr[i];

            arr[p-1]=v;
        n=n+1;
        }
        void del( int arr[])
        {
            int p;
            printf("\n Enter the position\n");
            scanf("%d",&p);

            for(i=p;i<=n;i++)
                arr[i-1]=arr[i];
        n=n-1;

        }
        void disp()
        {

                printf("\n\n************ ARRAY VALUES ARE *************\n\n ");
            for(i=0;i<n;i++)
            {
                printf( " arr[%d] :: %d\n ",i,arr[i]);
            }
        }




