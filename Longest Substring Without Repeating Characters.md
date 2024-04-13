# 3. Longest Substring Without Repeating Characters

## 說明
取出字串中，最常沒有重複字元的子句


## Code
```
class Solution {
public:
    int lengthOfLongestSubstring(string s) {
        string tmp = "", longStr = "";
        for(int i = 0; i < s.length(); ++i){
            for(int j = 0; j < tmp.length(); ++j){
                if(s[i] == tmp[j]) {
                    tmp.erase(0,j+1);
                }
            }
            tmp += s[i];

            if(tmp.length() > longStr.length()) {
                longStr = tmp;
            }
        }
        return longStr.length();
    }
};
```
