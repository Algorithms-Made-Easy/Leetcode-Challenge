class Solution {
    public int pivotIndex(int[] nums) {
        int total=0;
        for(int num:nums){
            total+=num;
        }

        int leftSum=0;
        for(int i=0;i<nums.length;i++){
            if(2*leftSum + nums[i] == total){
                return i;
            }
            leftSum+=nums[i];
        }
        return -1;
    }
}
