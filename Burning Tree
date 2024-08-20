class Solution{
    public static void dfs(Node root, Set<Node> set, int[] max, int currT){
        if (root == null || set.contains(root)) return;
        set.add(root);
        max[0] = Math.max(max[0], currT);
        dfs(root.left, set, max, currT + 1);
        dfs(root.right, set, max, currT + 1);
    }
    
    public static boolean pathT(Node root, int target, Queue<Node> q) {
        if(root == null) return false;
        if(root.data == target || pathT(root.left, target, q) || pathT(root.right, target, q)){
            q.offer(root);
            return true;
        }
        
        return false;
    }
    
    public static int minTime(Node root, int target){
        Queue<Node> q = new LinkedList<Node>();
        pathT(root, target, q);
        Set<Node> set = new HashSet<>();
        int time = 0;
        int[] max = new int[1];
        while (!q.isEmpty()) {
            dfs(q.poll(), set, max, time++);
        }
        
        return max[0];
    }
}
