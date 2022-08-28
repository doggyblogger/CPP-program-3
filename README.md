# CPP-program-3
Given a permutation of number from 1 to N. Among all the subarrays, find the number of unique pairs such that and a is maximum and b is second maximum in that subarray.


#include <bits/stdc++.h>
using namespace std;
int main()
{int n, ans = 0, a;
    stack <int> stk;
    cin >> n;
    for(int i=0;i<n;i++)
    {
        cin >> a;
        while(!stk.empty() and a > stk.top())
        {
            stk.pop();
            ans++;
        }
        if(!stk.empty()) 
        ans++;
        stk.push(a);
    }
    cout << ans << endl;
    return 0;
}
