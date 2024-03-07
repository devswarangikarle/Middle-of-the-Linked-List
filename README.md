# Middle-of-the-Linked-List
Given the head of a singly linked list, return the middle node of the linked list.  If there are two middle nodes, return the second middle node.

class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        slow_pointer = head
        fast_pointer = head

        while fast_pointer is not None and fast_pointer.next is not None:
            slow_pointer = slow_pointer.next
            fast_pointer = fast_pointer.next.next

        return slow_pointer
