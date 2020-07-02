### Question
Given a Linked list of size N, the list is in alternating ascending and descending orders. Your task is to complete the function sort() that sorts the given linked list in non-decreasing order.

#### Input:
2
6
1 9 2 8 3 7
5
13 99 21 80 50

#### Output:
1 2 3 7 8 9
13 21 50 80 99

### Answer

def sort(h1):
    read = h1
    write = h1
    datai = []
    
    while read:
        datai.append(read.data)
        read = read.next
    for i in sorted(datai):
        write.data = i
        write = write.next
    return h1
