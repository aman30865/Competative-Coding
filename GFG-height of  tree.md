### Question
Given a binary tree, find its height.

### Answer
def height(root):
    
    if root is None: 
        return 0 ;  
  
    else : 
  
        # Compute the depth of each subtree 
        lDepth = height(root.left) 
        rDepth = height(root.right) 
  
        # Use the larger one 
        if (lDepth > rDepth): 
            return lDepth+1
        else: 
            return rDepth+1
