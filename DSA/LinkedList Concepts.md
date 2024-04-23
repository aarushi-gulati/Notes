class Node:
	def __ init__(self, data):
		self.data = data
		self.next = None
		
class LinkedList:
	def __ init__ (self):
		self.head = None

## Reversing 
### Recursively 
def reverseUtil(self, curr, prev):
	if curr.next is None:
		self.head = curr
		curr.next = prev
		return
	next = curr.next
	curr.next = prev
	self.reverseUtil(next, curr)
def reverse(self):
	if self.head is None:
		return
	self.reverseUtil(self.head, None)

### Iteratively
def reverse(self):
    prev = None
    current = self.head
    while(current is not None):
        next = current.next
        current.next = prev
        prev = current
        current = next
    self.head = prev

## Floyd cycle detection - Loop removal and detection
def detectAndRemoveLoop(self):
	if not self.head or not self.head.next:
		return
	slow, fast = head, head
	while(fast and fast.next):
		slow = slow.next
		fast = fast.next.next
		if slow == fast:
			# this is where loop detection happens
			slow = head
			while(slow.next != fast.next):
				slow = slow.next
				fast = fast.next
			fast.next = None

Floyd cycle detection algorithm is also known as the Hare-Tortoise algorithm. 
It says that while traversing a list, one of the two things could occur:- 
* The fast pointer may reach NULL which shows there is no loop. 
* The fast pointer catches the slow pointer at some time therefore a loop exists in the linkedlist. 

Distance travelled by fast pointer = 2 * (Distance travelled  by slow pointer)  
  
(m + n* x + k) = 2* (m + n* y + k)  
  
Note that before meeting the point shown above, fast was moving at twice speed.  
  
x -->  Number of complete cyclic rounds made by   
       fast pointer before they meet first time  
  
y -->  Number of complete cyclic rounds made by   
       slow pointer before they meet first time

m + k = (x-2y)* n  
  
Which means  ***m+k is a multiple of n****.   
Thus we can write, m + k = i * n or **m = i * n - k****.  
Hence, distance moved by slow pointer: m, is equal to distance moved by fast pointer:  
i * n - k or (i-1) * n + n - k (cover the loop completely i-1 times and start from n-k).

So if we start moving both pointers again at ****same speed**** such that one pointer (say slow) begins from head node of linked list and other pointer (say fast) begins from meeting point. When the slow pointer reaches the beginning of the loop (has made m steps), the fast pointer would have made also moved m steps as they are now moving at the same pace. Since m+k is a multiple of n and fast starts from k, they would meet at the beginning. Can they meet before also? No because slow pointer enters the cycle first time after m steps.



