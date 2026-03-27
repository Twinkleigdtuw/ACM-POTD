class Solution {
public:
    bool checkIfExist(vector<int>& arr) {
        unordered_set<int> st;
        
        for (int x : arr) {
            if (st.count(2 * x)) return true;
            if (x % 2 == 0 && st.count(x / 2)) return true;
            
            st.insert(x);
        }
        
        return false;
    }
};
<img width="1835" height="826" alt="image" src="https://github.com/user-attachments/assets/7d5b2c35-b802-4be5-acbf-d105d8e27c55" />
