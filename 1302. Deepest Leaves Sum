class Solution {
    int sum  = 0;
    public int deepestLeavesSum(TreeNode root) {
        int maxDepth = maxDepth(root);
        findSum(root, 1, maxDepth);
        return sum;
    }
    
    public int maxDepth(TreeNode node) {
        if(node == null) return 0;
        return 1 + Math.max(maxDepth(node.left), maxDepth(node.right));
    }
    
    public void findSum(TreeNode node, int curr, int depth) {
        if(node != null) {
            if(curr == depth) {
                sum+=node.val;
            }
            findSum(node.left, curr+1, depth);
            findSum(node.right, curr+1, depth);
        }
    }
}


class Solution {
    int sum  = 0;
    int maxDepth = 0;
    public int deepestLeavesSum(TreeNode root) {
        findSum(root, 1);
        return sum;
    }
    
    
    public void findSum(TreeNode node, int curr) {
        if(node != null) {
            if(curr > maxDepth) {
                sum = 0;
                maxDepth = curr;
            }
            if(curr == maxDepth) {
                sum+=node.val;
            }
            findSum(node.left, curr+1);
            findSum(node.right, curr+1);
        }
    }
}
