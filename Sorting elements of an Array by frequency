class Solution {
    // Function to sort the array according to frequency of elements.
    public ArrayList<Integer> sortByFreq(int arr[]) {
        ArrayList<Integer> result=new ArrayList<>();
        HashMap<Integer,Integer> m=new HashMap<>();
         PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> {
            if (b[1] != a[1]) {
                return b[1] - a[1]; 
            } else {
                return a[0] - b[0]; 
            }
        });
        
        for(int i:arr) m.put(i,m.getOrDefault(i,0)+1);
        for(Map.Entry<Integer,Integer> me:m.entrySet()){
            pq.offer(new int[]{me.getKey(),me.getValue()});
        }   
        
         while(!pq.isEmpty()){
             int[] curr=pq.poll();
            int p=curr[1];
            while(p-->0){
                result.add(curr[0]);
            }
        }
        
        return result;
    }
}
