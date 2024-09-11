class Solution {
    // Function to return the minimum cost of connecting the ropes.
    public long minCost(long[] arr) {
        // code here
        
        PriorityQueue<Long> pq= new PriorityQueue<>();
        
        for(int i=0;i<arr.length;i++){
            pq.add( arr[i]);
        }
        
        long sum =0;
        
        while(pq.size()>1){
            long x=pq.poll();
            long y = pq.poll();
            
            sum += x+y;
            pq.add(x+y);
            
        }
        return sum;
    }
}
