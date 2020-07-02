#### Question

Get the sum of non-adjacent elements in a Binary Tree.(Sum of elements that are not directly connected)

#### Answer

def maxSumHelper(root) : 
  
    if (root == None):  
        sum = [0, 0]  
        return sum
      
    sum1 = maxSumHelper(root.left)  
    sum2 = maxSumHelper(root.right)  
    sum = [0, 0] 
  
    # This node is included (Left and right  
    # children are not included)  
    sum[0] = sum1[1] + sum2[1] + root.data  
  
    # This node is excluded (Either left or  
    # right child is included)  
    sum[1] = (max(sum1[0], sum1[1]) + 
              max(sum2[0], sum2[1]))  
  
    return sum
  
def maxSum(root) : 
  
    res = maxSumHelper(root)  
    return max(res[0], res[1]) 
