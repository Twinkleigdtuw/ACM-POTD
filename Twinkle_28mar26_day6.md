class Solution {
public:
    void rotate(vector<int>& nums, int k) {
        int n=nums.size();
        if(n==0) return ;
        k= k%n;
            reverse(nums.begin(), nums.end());
            reverse(nums.begin(), nums.begin()+k);
            reverse(nums.begin()+k, nums.end());                  
    }
};
<img width="1772" height="919" alt="image" src="https://github.com/user-attachments/assets/bf6de396-127e-4a91-900c-c5b92c9bda6e" />
