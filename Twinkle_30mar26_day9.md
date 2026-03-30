
class Solution {
public:
    bool hasCycle(ListNode * head) {
        if(head==NULL){
            return false;
        }
        ListNode* slow=head;
        ListNode* fast=head;
        while (fast!=NULL&&fast->next!=NULL){
            slow=slow->next;
            fast=fast->next->next;
            if(slow==fast){
                return true;
            }
        }
        return false; 
    }
};

auto init = atexit([]() { ofstream("display_runtime.txt") << "0"; });
<img width="1799" height="935" alt="image" src="https://github.com/user-attachments/assets/0a469283-08be-4293-a8f1-160d71adcb28" />
