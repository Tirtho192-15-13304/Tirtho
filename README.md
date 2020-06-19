#include<iostream>
using namespace std;
int main()
{
    int size,istart,jstart,temp;
    cin >> size;
    int inputArr[size];
    for(istart=0;istart<size;istart++)
    {
        cin >> inputArr[istart];
    }
    for(istart=0;istart<size-1;istart++)
    {
        for(jstart=0;jstart<size-1;jstart++)
        {
            if(inputArr[jstart]>inputArr[jstart+1]){
            temp =inputArr[jstart];
            inputArr[jstart]=inputArr[jstart+1];
            inputArr[jstart+1]=temp;
          }
        }
    }
    for(istart=0;istart<size;istart++)
    {
        cout << inputArr[istart] << endl;
    }
    int mid,start,end,data;
    cin >> data;
    for(istart=0;istart<size;istart++)
    {
        mid = istart+size/2;
        if(inputArr[mid]==data)
        {
            cout <<"Data Ffoud" << endl;
            cout << mid+1 << endl;
            break;
        }
        if(inputArr[mid]>data)
        {
            istart=mid-1;
        }
        else{
            size = mid+1;
        }

    }

}
