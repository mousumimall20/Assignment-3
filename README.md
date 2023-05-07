# Assignment-3
#Q1.Implement Binary tree

class Node:
    def _init_(self, val):
        self.val = val
        self.left = None
        self.right = None

class BinaryTree:
    def _init_(self, root_val):
        self.root = Node(root_val)
    
    def insert_left(self, parent, child_val):
        child = Node(child_val)
        parent.left = child
    
    def insert_right(self, parent, child_val):
        child = Node(child_val)
        parent.right = child
    
    def pre_order_traversal(self, node):
        if node is not None:
            print(node.val)
            self.pre_order_traversal(node.left)
            self.pre_order_traversal(node.right)
    
    def in_order_traversal(self, node):
        if node is not None:
            self.in_order_traversal(node.left)
            print(node.val)
            self.in_order_traversal(node.right)
    
    def post_order_traversal(self, node):
        if node is not None:
            self.post_order_traversal(node.left)
            self.post_order_traversal(node.right)
            print(node.val)
            
#Example:
# create the binary tree
tree = BinaryTree(1)
tree.insert_left(tree.root, 2)
tree.insert_right(tree.root, 3)
tree.insert_left(tree.root.left, 4)
tree.insert_right(tree.root.left, 5)

# traverse the binary tree
print("Pre-order traversal:")
tree.pre_order_traversal(tree.root)

print("In-order traversal:")
tree.in_order_traversal(tree.root)

print("Post-order traversal:")
tree.post_order_traversal(tree.root)
Pre-order traversal:
1
2
4
5
3
In-order traversal:
4
2
5
1
3
Post-order traversal:
4
5
2
3
1
#Q2.Find height of a given tree

class Node:
    def _init_(self, val):
        self.val = val
        self.left = None
        self.right = None

class BinaryTree:
    def _init_(self, root_val):
        self.root = Node(root_val)
    
    def insert_left(self, parent, child_val):
        child = Node(child_val)
        parent.left = child
    
    def insert_right(self, parent, child_val):
        child = Node(child_val)
        parent.right = child
    
    def height(self, node):
        if node is None:
            return 0
        else:
            left_height = self.height(node.left)
            right_height = self.height(node.right)
            return max(left_height, right_height) + 1

#Example:
# create the binary tree
tree = BinaryTree(1)
tree.insert_left(tree.root, 2)
tree.insert_right(tree.root, 3)
tree.insert_left(tree.root.left, 4)
tree.insert_right(tree.root.left, 5)

height = tree.height(tree.root)
print("Height of the tree is:", height)
Height of the tree is: 3
#Q3.Perform Pre-order, Post-order, In-order traversal

class Node:
    def _init_(self, val):
        self.val = val
        self.left = None
        self.right = None

class BinaryTree:
    def _init_(self, root_val):
        self.root = Node(root_val)
    
    def insert_left(self, parent, child_val):
        child = Node(child_val)
        parent.left = child
    
    def insert_right(self, parent, child_val):
        child = Node(child_val)
        parent.right = child
    
    def pre_order_traversal(self, node):
        if node is not None:
            print(node.val)
            self.pre_order_traversal(node.left)
            self.pre_order_traversal(node.right)
    
    def in_order_traversal(self, node):
        if node is not None:
            self.in_order_traversal(node.left)
            print(node.val)
            self.in_order_traversal(node.right)
    
    def post_order_traversal(self, node):
        if node is not None:
            self.post_order_traversal(node.left)
            self.post_order_traversal(node.right)
            print(node.val)
#Example:
# create the binary tree
tree = BinaryTree(1)
tree.insert_left(tree.root, 2)
tree.insert_right(tree.root, 3)
tree.insert_left(tree.root.left, 4)
tree.insert_right(tree.root.left, 5)
…
