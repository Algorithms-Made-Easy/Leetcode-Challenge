class Solution {
    public boolean isAlienSorted(String[] words, String order) {
        int[] mapping = new int[26];
        int seq=0;
        for(char ch:order.toCharArray()){
            mapping[ch-'a'] = seq++;
        }
        
        for(int i=0;i<words.length - 1;i++){
            String curr = words[i];
            String next = words[i+1];
            
            int len = Math.min(curr.length(),next.length());
            
            if(len!= curr.length() && len == next.length() && curr.startsWith(next)){
                return false;
            }
            
            for(int l=0;l<len;l++){
                if(mapping[curr.charAt(l)-'a'] > mapping[next.charAt(l)-'a']){
                    return false;
                }
                
                if(mapping[curr.charAt(l)-'a'] < mapping[next.charAt(l)-'a']){
                    break;
                }
                
            }
        }
        
        return true;
    }
}
