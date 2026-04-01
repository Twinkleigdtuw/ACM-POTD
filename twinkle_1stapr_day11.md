class Solution {
public:
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {
        ListNode* dummy = new ListNode(-1);
        ListNode* temp = dummy;
        while (list1 != NULL && list2 != NULL) {
            if (list1->val <= list2->val) {
                temp->next = list1;
                list1 = list1->next;
            } else {
                temp->next = list2;
                list2 = list2->next;
            }
            temp = temp->next;
        }
        if (list1 != NULL) {
            temp->next = list1;
        } else {
            temp->next = list2;
        }
        return dummy->next;
    }
};

<img width="1592" height="837" alt="image" src="https://github.com/user-attachments/assets/753e38b0-4ac7-4652-8372-8a8ab762683c" />
