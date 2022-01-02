# 1602B---Codeforces

#include <stdio.h>

int main()
{
    int t;
    scanf("%d",&t);
    while(t--){
        int n;
        scanf("%d",&n);
        int a[n],aux[n];
        for(int i=0;i<n;i++){
            scanf("%d",&a[i]);
            aux[i]=a[i];
        }
        int q,x,k,i;
        scanf("%d",&q);
        for(int l=0;l<q;l++){
            scanf("%d",&x);
            scanf("%d",&k);
            for(int p=0;p<k;p++){
                for(i=0;i<n;i++){
                    int count=0;
                    for(int j=0;j<n;j++){
                        if(a[i]==a[j]){
                            count++;
                        }
                    }
                    aux[i]=count;
                }
                for(int l=0;l<n;l++){
                    a[l]=aux[l];
                }
            }
            printf("\n%d\n",aux[x]);
        }
    }
}
