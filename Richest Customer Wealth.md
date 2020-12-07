## Description
You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the ith customer has in the jth bank. Return the wealth that the richest customer has.
A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.


## Code
```cpp
class Solution {
public:
    int maximumWealth(vector<vector<int>>& accounts) {
        int max = 0;
        for(int i = 0; i< accounts.size(); ++i) {
            int tmp = 0;
            for(int j = 0; j < accounts[i].size(); ++j) {
                tmp += accounts[i][j];
            }
            if (tmp > max) 
                max = tmp;
        }
        return max;
    }
};
```
