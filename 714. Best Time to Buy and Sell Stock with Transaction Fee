class Solution {
    public int maxProfit(int[] prices, int fee) {
        //O(1) - Space
        int n = prices.length;
        int profit = 0; 
        int effectiveBuyPrice = prices[0];
        
        
        //O(N) - Time
        for(int i = 1; i < n; i++) {
            profit = Math.max(profit, prices[i]-effectiveBuyPrice-fee);
            effectiveBuyPrice = Math.min(effectiveBuyPrice, prices[i]-profit);
        }
        
        return profit;
    }
}
