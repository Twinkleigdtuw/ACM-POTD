class Solution {
public:
    bool isPalindrome(ListNode* head) {
        stack<int>rev;
        ListNode* temp= head;
        while (temp!=NULL){
            rev.push(temp -> val);
            temp=temp->next;
        }
        temp=head;
        while (temp!=NULL){
            if (temp->val!= rev.top())return false;
            rev.pop();
            temp=temp->next;
        }
        return true;
    }
};
<img width="1698" height="948" alt="image" src="https://github.com/user-attachments/assets/be45495c-e02c-4aa7-9048-e3ac13d2562b" />
