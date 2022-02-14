# list_problems
list problems with their different solving method
'''
##1. Write a Python program to sum all the items in a list.
import math
list = [1,-2,3,-4,-5,6,7,8,-9]
sum_of_list = print(sum(list))

##or another way
def sum_list(items):
    sum_numbers=0
    for x in items:
        sum_numbers += x
    return sum_numbers
print(sum_list([1,-2,3,-4,-5,6,7,8,-9]))

_____________________________________________________________
##2: Reverse a list in Python
h = [1,2,3,4,5,6,7,8]
h.reverse()
print(h)

_____________________________________________________________-

##3: Concatenate two lists index-wise
l1 = ["M", "na", "i", "Ke"]
l2 = ["y", "me", "s", "lly"]
final = print([(l1[0] + l2[0] ) + ' ' +(l1[1] + l2[1]) +' ' +(l1[2]+l2[2])+ ' '+ (l1[3 ]+l2[3])])
print(final)
             #or
mapped = [list(zip(l1,l2))]
print(mapped)

_____________________________________________________________-

##3: Turn every item of a list into its square

n = [1, 2, 3, 4, 5, 6, 7]

squars = [x**2 for x in n]
print(squars)

#or
res = []
for i in n:
 res.append(i * i)
print(res)

_____________________________________________________________-

##6: Iterate both lists simultaneously
list1 = [10, 20, 30, 40]
list2 = [100, 200, 300, 400]

for x,y in zip(list1,list2[::-1]):
 print(x,y)

____________________________________________________________________
##7: Remove empty strings from the list of strings
list1 = ["Mike", "", "Emma", "Kelly", "", "Brad"]

del list1[1],list1[3]
print(list1)

#or

r = list(filter(None,list1))
print(r)
______________________________________________________________________________________


## 8: Add new item to list after a specified item

list1 = [10, 20, [300, 400, [5000, 6000], 500], 30, 40]

list1[2][2].append(7000)
print(list1)

_____________________________________________________________________

##9: Extend nested list by adding the sublis

list1 = ["a", "b", ["c", ["d", "e", ["f", "g"], "k"], "l"], "m", "n"]
#        a=0     b=1    c=2(1)  d=2(1)[0]   f=2(1)[2]
sub_list = ["h", "i", "j"]

list1[2][1][2].extend(sub_list)
print(list1)

_____________________________________________________________________________________

##10: Replace list’s item with new value if found

list1 = [5, 10, 15, 20, 25, 50, 20]

list1[3]=200
print(list1)

#or

list1.insert(20,200)
print(list1)

#or
index = list1.index(20)
list1[index] = 200
print(list1)

___________________________________________________________________________________

##11: Remove all occurrences of a specific item from a list.

list1 = [5, 20, 15, 20, 25, 50, 20]

del list1[1]
del list1[2]
del list1[4]

print(list1)

#or
#using fun
def remove_val(sample_list,val):
    return [i for i in sample_list if i != val]
res = remove_val(list1,20)
print(res)

#or
#using while loop
while 20 in list1:
    list1.remove(20)
print(list1)

_________________________________________________

##12. Write a Python program to sum all the items in a list.
sum_list = [1,2,-8]

total = sum(sum_list)

print(total)

#or

def sum_list(items):
    sum_number=0
    for x in items:
        sum_number += x
    return sum_number

print(sum_list([1,2,-8]))

________________________________________________________________

##13. Write a Python program to multiply all the items in a list.
import math
list1 = [1,2,-8]
r = math.prod(list1)
print(r)

#or

from functools import reduce
list1 = [1,2,-8]

r2 = reduce((lambda x, y: x * y),list1)
print(r2)

#or

def mul(mylist):
    result = 1
    for x in mylist:
        result = result *x
    return result
list1 = [1,2,-8]
print(mul(list1))

______________________________________________________________

##14. Write a Python program to get the largest number from a list.

max_num_in_list= [1, 2, -8, 0]

largest = max(max_num_in_list)

print(largest)

#or

max_num_in_list.sort()

print('largest no. is :',max_num_in_list[-1])

#or

def max_num_in_list( list ):
    max = list[ 0 ]
    for a in list:
        if a > max:
            max = a
    return max
print(max_num_in_list([1, 2, -8, 0]))

'''









































