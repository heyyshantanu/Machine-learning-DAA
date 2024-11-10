#include<bits/stdc++.h>
using namespace std;

void print(int n,int col[])     
{
        for(int i=0;i<n;i++)
        {
               for(int j=0;j<n;j++)
               {
                
                        if(col[i]==j) cout<<i+1<<" ";
                        else cout<<"0 ";
               }
               cout<<"\n";
        }
        cout<<"\n";      
}


bool place(int queen,int c,int col[])     
{
        int j=0;
        while(j<queen)
        {
                if(col[j]==c || abs(col[j]-c)==abs(j-queen))    
                        return false;
                j++;
        }
        return true;
}

bool nqueen(int queen,int n,int col[])  
{
        int fl=0;
        
        for(int i=0;i<n;i++)
        {
                if(place(queen,i,col))
                {
                        col[queen]=i;   
                        
                        cout<<"Placing Queen "<<queen+1<<"\n";
                        print(n,col);
                        
                        if(queen==n-1) return true;
                        
                        if(nqueen(queen+1,n,col))
                                return true;
                        
                        col[queen]=-1;
                        
                        cout<<"Backtracking Queen "<<queen+1<<"\n";
                        print(n,col);
                        
                       
                        fl=1;
                }
                        
        }       
        
        if(!fl)
        cout<<"Unable to place Queen "<<queen+1<<"\n\n";
        
        return false;
}



int main()
{
        int n;
        cout<<"Enter Size of chessboard : ";
        cin>>n;
        
        if(n<=3)
        {
                cout<<"\nSize should be more than 3\n";
                return 0;
        }
        
        
        int col[n];
        for(int i=0;i<n;i++) col[i]=-1;
        
        nqueen(0,n,col);
          
        return 0;
}
