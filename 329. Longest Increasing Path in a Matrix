class Solution {
    int[][] dir = {{1,0}, {-1,0}, {0,1}, {0,-1}};
    public int longestIncreasingPath(int[][] matrix) {
        if(matrix == null || matrix.length == 0) return 0;
        int m = matrix.length, n = matrix[0].length;
        int[][] mem = new int[m][n];
        int longestPath = 0;
        
        for(int i = 0; i < m; i++) {
            for(int j = 0; j < n; j++) {
                int path = dfs(matrix, m, n, i, j, mem);
                longestPath = Math.max(path, longestPath);
            }
        }
        
        return longestPath;
    }
    
    public int dfs(int[][] matrix, int m, int n, int i, int j, int[][] mem) {
        if(mem[i][j] > 0) return mem[i][j];
        int max = 0;
        for(int[] d : dir) {
            int x = i+d[0], y = j+d[1]; 
            if(x >= 0 && y >= 0 && x < m && y < n && matrix[x][y] > matrix[i][j]) {
                max = Math.max(max, dfs(matrix, m, n, x, y, mem));
            }
        }
        mem[i][j] = max+1;
        return max+1;
    }
}
