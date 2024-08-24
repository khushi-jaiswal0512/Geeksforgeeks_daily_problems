class Solution {
    // Function to return max value that can be put in knapsack of capacity W.
    static int knapSack(int W, int wt[], int val[]) {
       int n = val.length;
        int maxValue = 0;

   
        for (int i = 0; i < n; i++) {
          
            if (wt[i] <= W) {
                maxValue = Math.max(maxValue, val[i]);
            }

            for (int j = i + 1; j < n; j++) {
               
                int totalWeight = wt[i] + wt[j];
                int totalValue = val[i] + val[j];

                if (totalWeight <= W) {
                    maxValue = Math.max(maxValue, totalValue);
                }

                for (int k = j + 1; k < n; k++) {
                
                    totalWeight = wt[i] + wt[j] + wt[k];
                    totalValue = val[i] + val[j] + val[k];

                    if (totalWeight <= W) {
                        maxValue = Math.max(maxValue, totalValue);
                    }
                }
            }
        }

        return maxValue;
    }
}
