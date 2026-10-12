/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
ListNode current = headA;

while (current != null) {
    ListNode second = headB;

    while (second != null) {
        if (current == second) {
            return current;
        }

        second = second.next;
    }

    current = current.next;
}
return null;
    }
}
