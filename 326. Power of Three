class Solution {
    public boolean isPowerOfThree(int n) {
        //27 27/3=9(0) --> 9/3=3(0) --> 3/3=1(0)  --> n has reduced to 1
        //10 10/3=3(1) --> false (remainder != 0)
        
        while(n>=3) {
            if(n%3 != 0) return false;
            n=n/3;
        }
        return n==1;
    }
}
