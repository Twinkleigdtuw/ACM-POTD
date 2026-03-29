class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode* prev=NULL;
        ListNode* curr=head;
        ListNode* next=NULL;
        while(curr!=NULL){
            next=curr->next;
            curr->next=prev;
            prev=curr;
            curr=next;
        }        
        return prev;
    }
};
<img width="1842" height="939" alt="image" src="https://github.com/user-attachments/assets/d9d5a774-2a85-4c6a-9bea-bdb4e62f9ec8" />
