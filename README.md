#include<bits/stdc++.h>
using namespace std;
int f(int n)
{
      if(n==1)
                return 1;
      return n*f(n-1);
}
int main(){
        int n,a[10001],sum=0;
        cin>>n;
        for(int i=0;i<n;i++){
                cin>>a[i];
        }
        for(int i=0;i<n-1;i++){
                int cnt=0;
                for(int j=i+1;j<n;j++){
                        if(a[j]<a[i]){
                                cnt++;
                        }
                }
                sum+=cnt*f(n-i-1);
        }
        cout<<sum<<endl;
        if(next_permutation(a,a+n)){
                for(int i=0;i<n;i++){
                        cout<<a[i]<<" ";
                }
                cout<<endl;
        }
}
