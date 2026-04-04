class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        if (head == NULL) return head;
        ListNode* current = head;
        while (current != NULL && current->next != NULL) {
            if (current->val == current->next->val) {
                current->next = current->next->next;
            } else {
                current = current->next;
            }
        }
        return head;
    }
};
<img width="1854" height="963" alt="image" src="https://github.com/user-attachments/assets/573fbf33-58c5-4eaa-8225-6bd8c638f22c" />
