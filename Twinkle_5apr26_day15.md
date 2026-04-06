class Solution {
public:
    bool isValid(string s) {
        stack<char>st;
        for(char c:s){
            if (c=='(' || c=='{' || c=='['){
                st.push(c);
            }
            else{
                if (st.empty()) return false;
                char top=st.top();
                st.pop();
                if ((c==')' && top!='(' )|| (c=='}'&&top!='{')||(c==']'&&top!='[')){
                return false;
                }
            }
        }
        return st.empty();
    }    
};
<img width="1895" height="642" alt="image" src="https://github.com/user-attachments/assets/0ebc19f7-f10a-4d71-8752-8da78624625b" />
