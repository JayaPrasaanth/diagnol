#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int n, a, i;
    int ft,st;
    int f=0,s=0,sum=0;
    cin>>n;
    ft=1;
    st=n;
    for(i=1;i<=(n*n);i++)
     {
        cin>>a;
        if(i==ft)
         {
            f += a;
            ft += n+1;   
         }
        if(i==st && st!=(n*n))
         {
           s += a;
           st += n-1;
         }
     } 
    sum = abs(f-s);
    cout<<sum;   
    return 0;
}
