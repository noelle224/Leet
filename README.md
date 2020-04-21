# Leet
Leetcode
https://leetcode.com/problems/best-time-to-buy-and-sell-stock/
# code solution

 
 
 
      public int maxProfit(int[] prices) 
     {
       
       int n=prices.length;
       if(n==0)
           return 0;
        int profit=0;
        int dp[]=new int[n+1];
        dp[0]=prices[0];
        for(int i=1;i<n;i++)
        {
           dp[i]=Math.min(dp[i-1],prices[i]);
            profit=Math.max(profit,prices[i]-dp[i]);
            
        }
        return profit;
        
    }
