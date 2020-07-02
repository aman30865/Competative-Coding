### Question
Check if given tree is a BST

### Answer

def isBST(node):

    return (isBSTUtil(node, INT_MIN, INT_MAX))

  #Return true if the given tree is a BST and its values are >= min and <= max
  
  def isBSTUtil(node, mini, maxi):
    
    # An empty tree is BST
    if node is None:
        return True

    # False if this node violates min/max constraint
    if node.data < mini or node.data > maxi:
        return False

    # Otherwise check the subtrees recursively
    # tightening the min or max constraint
    return (isBSTUtil(node.left, mini, node.data -1) and
          isBSTUtil(node.right, node.data+1, maxi))
