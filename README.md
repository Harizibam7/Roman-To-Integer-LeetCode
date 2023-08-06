# Roman-To-Integer-LeetCode

Roman to Integer in LeetCode by using C++

    #include <map>
    #include <unordered_map>
    class Solution {
    public:
        int romanToInt(string s) {
            map<char,int> roman;
            roman.insert(make_pair('I',1));
            roman.insert(make_pair('V',5));
            roman.insert(make_pair('X',10));
            roman.insert(make_pair('L',50));
            roman.insert(make_pair('C',100));
            roman.insert(make_pair('D',500));
            roman.insert(make_pair('M',1000));
    
            int result =0;
    
            for(int i= s.length()-1;i>=0;i--){
                if(roman[s[i]]<roman[s[i+1]]){
                    result-=roman[s[i]];
                }
                else{
                    result+=roman[s[i]];
                }
    
            }
            return result;
    
    
    
    
        }
    };
