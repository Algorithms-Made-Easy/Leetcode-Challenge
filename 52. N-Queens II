class Solution {
    int count;
    public int totalNQueens(int n) {
        count = 0;
        List<int[]> queens = new ArrayList<>();
        dfs(n, 0, queens);
        return count;
    }
    
    private void dfs(int n, int row, List<int[]> queens) {
        if(queens.size() == n) {
            count++;
            return;
        }
        for(int col = 0; col < n; col++) {
            if(canPlaceQueen(row, col, queens)) {
                queens.add(new int[]{row, col});
                dfs(n, row+1, queens);
                queens.remove(queens.size()-1);
            }
        }
    }
    
    private boolean canPlaceQueen(int row, int col, List<int[]> queens) {
        for(int[] q : queens) {
            int dx = Math.abs(q[0] - row);
            int dy = Math.abs(q[1] - col);
            if(dx == 0 || dy == 0 || dx == dy) return false;
        }
        return true;
    }
}
