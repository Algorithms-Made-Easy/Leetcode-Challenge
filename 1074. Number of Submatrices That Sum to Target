class Solution {
    public int numSubmatrixSumTarget(int[][] matrix, int target) {
        int m = matrix.length,n=matrix[0].length;
        
        for(int row =0;row<m;row++){
            for(int col=1;col<n;col++){
                matrix[row][col]+=matrix[row][col-1];
            }
        }
        
        int count=0;
        
        for(int c1=0;c1<n;c1++){
            for(int c2=c1;c2<n;c2++){
                
                Map<Integer,Integer> map = new HashMap<>();
                map.put(0,1);
                int sum=0;
                
                for(int row=0;row<m;row++){
                    sum += matrix[row][c2] - (c1>0 ? matrix[row][c1-1] : 0);
                    count += map.getOrDefault(sum-target,0);
                    map.put(sum,map.getOrDefault(sum,0)+1);
                }
                
            }
        }
        
        return count;
    }
}
