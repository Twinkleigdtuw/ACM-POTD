class Solution {
public:
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
        if (headA == NULL || headB == NULL) return NULL;
        ListNode* a = headA;
        ListNode* b = headB;
        while (a != b) {
            a = (a == NULL) ? headB : a->next;
            b = (b == NULL) ? headA : b->next;
        }
        return a; 
    }
};
<img width="1834" height="1025" alt="image" src="https://github.com/user-attachments/assets/ce632217-ec59-4f42-8b57-a7dbc81ee326" />
