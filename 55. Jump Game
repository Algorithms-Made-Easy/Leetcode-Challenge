class Solution {
    public boolean canJump(int[] nums) {
        int n = nums.length;
        
        if(n==1) return true;
        
        int max = 0;
        
        for(int index=0;index<n-1 && max>=index;index++){
            if(max<index+nums[index]){
                max = index + nums[index];
            }
            
            if(max>=n-1){
                return true;
            }
        }
        
        return false;
    }
}
