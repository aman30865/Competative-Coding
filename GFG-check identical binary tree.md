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
    
