code-
=====
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int a[10], b[10],i=0, c[10], n,k,max=0,u,l=0,e,m=0,x=0,v=0,d,r;
    scanf("%d", &n);
    k=n;
    while(k>0) {
        a[i]=k%10;
        k=k/10;
        i++;
    }
    e=i;
    while(l<e) {
        i--;
        while(i>=0) {
            if(a[i]>0) {
                if(a[i]>max) {
                    max=a[i];
                    u=i;
                }
                i--;
            } else {
                i--;
            }
        }
        i=e;
        b[l]=max;
        max=0;
        a[u]=-1;
        l++;
    }
    while(x<e) {
        m=m*10+b[x];
        x++;
    }
    x=0;
    i--;
    while(x<e) {
        if(x==0&&b[i]==0) {
            c[1]=b[i];
        } else {
            if(x==1) d=x-1;
            else d=x;
            c[d]=b[i];
        }
        x++;
        i--;
    }
    x=0;
    while(x<e) {
        v=v*10+c[x];
        x++;
    }
    r=v+m;
    printf("%d", r);
    return 0;
}

code?
