# DSA-Remove-Duplicates-from-Sorted-List
Given the head of a sorted linked list, delete all duplicates such that each element appears only once. Return the linked list sorted as well.

```
Input: head = [1,1,2]
Output: [1,2]
```
```
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def deleteDuplicates(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head is None:
            return head
        current=head.next
        prev=head
        while current:
            if current.val==prev.val:
                prev.next=current.next
                current=current.next
            else:
                current=current.next
                prev=prev.next
        return head

```
