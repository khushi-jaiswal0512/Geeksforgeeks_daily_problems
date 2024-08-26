class Solution {
    public int wildCard(String ptr, String str) {
        ptr="$"+ptr;
        str="$"+str;
        
        Boolean dp[][]=new Boolean[ptr.length()+1][str.length()+1];
        
        dp[0][0]=true;
        for(int i=1;i<dp.length;i++)dp[i][0]=false;
        for(int j=1;j<dp[0].length;j++)dp[0][j]=false;
        
        
        for(int i=1;i<dp.length;i++){
            for(int j=1;j<dp[0].length;j++){
                    if(str.charAt(j-1)==ptr.charAt(i-1) || ptr.charAt(i-1)=='?'){
                         dp[i][j]= dp[i-1][j-1]; 
                    }else if(ptr.charAt(i-1)=='*'){
                        dp[i][j]=dp[i][j-1] || dp[i-1][j];
                    }else {
                        dp[i][j]=false;
                    }
            }
        }
        return dp[dp.length-1][dp[0].length-1]==true?1:0;
    }
}
