#include <stack>
using namespace std;

class MyQueue {
public:
    stack<int> st;
    void push(int x) {
        stack<int> temp;
        while (!st.empty()) {
            temp.push(st.top());
            st.pop();
        }
        st.push(x);
        while (!temp.empty()) {
            st.push(temp.top());
            temp.pop();
        }
    }
    int pop() {
        int val = st.top();
        st.pop();
        return val;
    }
    int peek() {
        return st.top();
    }
    bool empty() {
        return st.empty();
    }
};
<img width="1853" height="936" alt="image" src="https://github.com/user-attachments/assets/1eaac7ee-ea26-4b04-8d98-17bab81b9be2" />
