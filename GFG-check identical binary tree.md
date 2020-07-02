### Question
Given two binary trees, the task is to find if both of them are identical or not. 

### Answer
def isIdentical(root1, root2):
    
    tr1 = []
    tr2 = []
    def inorderd(root,tr):
        if root:
            inorderd(root.left,tr)
            tr.append(root.data)
            inorderd(root.right,tr)
        else:
            tr.append("NULL")
    inorderd(root1,tr1)
    inorderd(root2,tr2)
    if tr1 == tr2:
        return True
    else:
        return False
#### Alt. Answer
def isIdentical(root1,root2):
    
    def isIdentical(root1, root2):
    
    if root1 == None and root2 == None:
        return True
    if root1 and root2:
        return (True if root1.data == root2.data else False) and isIdentical(root1.left,root2.left) and isIdentical(root1.right,root2.right)
    return False
