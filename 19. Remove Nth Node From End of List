/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode dummy =new ListNode(0);
        dummy.next = head;
        ListNode current = dummy, nth = dummy;
        
        for(int i=1;i<=n+1;i++){
            current = current.next;
        }
        
        while(current!=null){
            current = current.next;
            nth = nth.next;
        }
        
        nth.next = nth.next.next;
        
        return dummy.next;
    }
}
