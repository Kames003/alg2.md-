# Algoritmy 2 

```cpp
#include <iostream>
#include <unordered_map>
#include <vector>
using namespace std;

int findModus(const vector<int> &arr)
{
    // ! implementataion using the hash map
    unordered_map<int, int> freqMap; // hash mapa na uchovanie četnosti
    int maxFreq = 0;                 // varka na maxfreq
    int modus = arr[0];              // ! varka na najvyššiu četnsot

    // ? range based for loop
    for (int num : arr)
    {
        freqMap[num]++; // ? inkriminacia
                        // ! pokiaô prevrši tak to setne
        if (freqMap[num] > maxFreq)
        {
            maxFreq = freqMap[num];
            modus = num;
        }
    }

    return modus;
}

int main()
{
    // ! vstupne data
    vector<int> arr = {1, 3, 2, 3, 4, 5, 3, 1, 1, 1};
    cout << "Modus je: " << findModus(arr) << endl;
    return 0;
}
```
