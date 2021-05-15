class Solution {
    public boolean isNumber(String s) {
        boolean digitseen =false, eseen = false, dotseen=false;
        int countPlusMinus = 0;
        
        for(int i=0;i<s.length();i++){
            char ch = s.charAt(i);
            
            //digit
            if(Character.isDigit(ch)){
                digitseen = true;
            }
            //minus/plus
            else if(ch =='+' || ch == '-'){
                if(countPlusMinus == 2){
                    return false;
                }
                
                if(i>0 && (s.charAt(i-1) != 'e' && s.charAt(i-1) != 'E')){
                    return false;
                }
                
                if(i == s.length()-1){
                    return false;
                }
                
                countPlusMinus++;
            }
            //dot
            else if(ch == '.'){
                if(eseen || dotseen){
                    return false;
                }
                
                if(i == s.length() -1 && !digitseen){
                    return false;
                }
                
                dotseen = true;
            }
            
            //e/E
            else if(ch == 'e' || ch == 'E'){
                if(eseen || !digitseen || i == s.length()-1){
                    return false;
                }
                
                eseen = true;
            }
            else{
                return false;
            }
            
        }
        
        return true;
    }
}
	
import java.util.regex.*;
class Solution {
    public boolean isNumber(String s) {
        return Pattern.matches("^([+-]?(((\\d+\\.\\d*)|(\\.\\d+))|(\\d+))([eE][+-]?\\d+)?)$", s);
    }
    
}
