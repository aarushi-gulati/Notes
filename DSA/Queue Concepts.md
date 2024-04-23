## Implementation from scratch
class Queue:
	def __ init__(self, capacity):
		self.front = 0
		self.rear = -1
		self queue = [None] * capacity
		self.size = 0
	def isFull(self):
		return self.size == self.capacity
	def isEmpty(self):
		return self.size == 0 
	def enqueue(self, val):
		