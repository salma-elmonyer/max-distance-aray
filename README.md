#include<iostream>
#include<climits>
using namespace std;

int maxDistance(int A[], int n){
        
        int dmax = INT_MIN;
        for(int i =0; i < n; i++){
            for(int j=0; j<n; j++){
                if(i !=j){
                    int diff = A[i] - A[j];
                    if(diff < 0){
                        diff = -diff;
                    }
                    if(diff > dmax){
                        dmax = diff;
                    }
                }
            }
        }
        return dmax;
    }

int main(){
    int n = 4;
    int A[n];
    cout << "enter a number of numbers: ";
    for(int i = 0; i < n; i++){
        cin >> A[i];
    }
    int result = maxDistance(A,n);
    cout << "the max diffirance is: " << result;
    
}
