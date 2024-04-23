## Implementation from scratch
class Stack:
	def __ init__ (self):
		self.stack = [-1] * size
		self.top = -1
	def push(self, val):
		top += 1
		self.stack.append(val)
	def isEmpty(self):
		return self.top == -1
	def peek(self):
		if self.isEmpty:
			return None
	def pop(self):
		if self.isEmpty():
			return None
		self.top -= 1
		return self.stack.pop()
	