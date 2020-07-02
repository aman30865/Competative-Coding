### Question
You are given a pointer/ reference to the node which is to be deleted from the linked list of N nodes. The task is to delete the node. Pointer/ reference to head node is not given. 

#### Input:
First line of input contains number of testcases T. For each testcase, first line of input contains length of linked list and next line contains the data of the linked list. The last line contains the node to be deleted.

#### Output:
For each testcase, in a newline, print the linked list after deleting the given node.

#### Input:
2
2
1 2
1
4
10 20 4 30
20
#### Output:
2
10 4 30

### Answer
def deleteNode(curr_node):

    next_node = curr_node.next
    last_node = next_node.next
    curr_node.data = next_node.data
    curr_node.next = last_node
