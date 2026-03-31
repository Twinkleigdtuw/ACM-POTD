class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        ListNode* slow= head;
        ListNode* fast = head;
        while (fast && fast->next){
            slow=slow->next;
            fast= fast->next->next;
        }
        return slow;
    }
};
<img width="1888" height="967" alt="image" src="https://github.com/user-attachments/assets/f2f0979a-94c8-41b1-be5b-47c657102285" />
