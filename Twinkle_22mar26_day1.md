class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if (nums.empty()) return 0;
        int i =0;
        for (int j=1; j<nums.size(); j++){
            if (nums[j]!=nums[i]){
                i++;
                nums[i]=nums[j];
            }
        }
        return i+1;
    }
};
<img width="775" height="682" alt="image" src="https://github.com/user-attachments/assets/0d4e449d-2e0c-4080-8b22-1b5f4d79813f" />
