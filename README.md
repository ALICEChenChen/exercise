//# exercise
//the first time use of GitHub
#include <stdio>
#include <iostream>

using namespace std;

int AdjusttArray(int s[], int l, int r) 
{  
    int i = l, j = r;  
    int x = s[l];
    while (i < j)  
    {  
       
        while(i < j && s[j] >= x)   
            j--;    
        if(i < j)   
        {  
            s[i] = s[j]; 
            i++;  
        }  
  
        
        while(i <j &&  s[i] < x)  
            i++;    
        if(i<j)
        {  
            s[j] = s[i]; 
            j--;  
        }  
    }  
   
    s[i] = x;  
  
    return i;  
}  

int main()
{
int array10]=[2,4,3,6,7,8,5,3,2,1];
AdjusttArray(array,1,9);
for(int i=0;i<10;i++)
{
cout<<array[i]<<endl;
}
return 0;
}
