class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int n=nums.size();
        int actual=0;
        int exp=(n*(n+1))/2;
        for(int num:nums){
            actual+=num;
        }
        return exp-actual;
    }
};
<img width="1785" height="972" alt="image" src="https://github.com/user-attachments/assets/f5cba993-f9c2-48d3-a807-3d9e1cf946c7" />
