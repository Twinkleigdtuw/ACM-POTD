class Solution {
public:
    int maxProfit(vector<int>& prices) {
        int minprice = INT_MAX;
        int maxprofit = 0;
        for (int i = 0; i < prices.size(); i++) {
            if (prices[i] < minprice) {
                minprice = prices[i];  
            } else {
                int profit = prices[i] - minprice;
                maxprofit = max(maxprofit, profit);
            }
        }
        return maxprofit;
    }
};
<img width="1870" height="995" alt="image" src="https://github.com/user-attachments/assets/bae251f1-1049-4af6-ae1d-a7190c1781f6" />
