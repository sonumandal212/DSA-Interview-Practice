


```cpp

#include <bits/stdc++.h>
using namespace std;

void
insertion_sort (int arr[],int i, int n)
{
  //base case
    if(i == n)
        return ;
    for(int j = i+1 ; j < n;j++){
        if(arr[i]>arr[j])
            swap(arr[i],arr[j]);
    }
    insertion_sort(arr,i+1,n);
}


int
main ()
{
  int n;
  cin >> n;


  int arr[n];

  for (int i = 0; i < n; i++)
    {
      cin >> arr[i];
    }

  insertion_sort (arr,0, n);

  for (int i = 0; i < n; i++)
    {
      cout << arr[i] << " ";
    }

  return 0;
}

```