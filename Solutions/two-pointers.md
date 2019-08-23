## 1.Two Sum 
`Easy`

#### 问题描述：
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

**Example**
> Given nums = [2, 7, 11, 15], target = 9,
>
> Because nums[0] + nums[1] = 2 + 7 = 9,  
> return [0, 1].

#### Solutions：
1. 此题是对有序数组进行求和，因此可以直接使用Two Pointers进行求解。
2. 还可以使用Hash Table进行求解，将每个数存入键值对中，遍历每个值，求target - 当前值是否在键值对中。


## 19. Remove Nth Node From End of List
`Medium`

#### 问题描述：
Given a linked list, remove the n-th node from the end of list and return its head.

**Example:**
> Given linked list: 1->2->3->4->5, and n = 2.
>
> After removing the second node from the end, the linked list becomes 1->2->3->5.

**Note:**
Given n will always be valid.

#### Solutions：
1. 此题需要找到倒数第n个结点，并删除它，因此可以使用Two Pointers，让fast pointer和low pointer相距n，当fast pointer走到链表的末尾，low pointer便到了倒数第n个位置，但是还使用一个变量需要保存low pointer的前一个结点的指针，便于删除low pointer指向的结点。
2. 对于一些边界条件，比如空链表、一个结点的链表，


## 26. Remove Duplicates from Sorted Array
`Easy`

#### 问题描述：
Given a sorted array nums, remove the duplicates in-place such that each element appear only once and return the new length.

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

```
Example 1:
Given nums = [1,1,2],

Your function should return length = 2, with the first two elements of nums being 1 and 2 respectively.

It doesn't matter what you leave beyond the returned length.
```

```
Example 2:
Given nums = [0,0,1,1,1,2,2,3,3,4],

Your function should return length = 5, with the first five elements of nums being modified to 0, 1, 2, 3, and 4 respectively.

It doesn't matter what values are set beyond the returned length.
```

#### Solutions：
分析：算法要求O(1)的空间复杂度，因此不能创建新的数组，只能在现有的数组上进行操作。

思路：
1. 把第i个新的数字到赋为nums[i]的值，即设置一个指针记录当前不同数字的个数，便于将值赋予相应的位置，另一个指针遍历数组。因为如果直接移除数字的话，会使得数组发生变化，迭代器失效，无法继续进行迭代。
若交换的话，需要创建一个新的变量判断后一个数字是否与前一个数字相同。

#### Codes:
```
int removeDuplicates(vector<int>& nums) {
        if (nums.empty()) {
            return 0;
        }
        int num = 1;
        for (auto it = ++nums.begin(); it != nums.end(); it++) {
            if (*it != *(it - 1)) {
                *(nums.begin() + num) = *it;
                // swap(*(nums.begin() + num), *it);
                num++;
            }
        }
        return nums;
    }
```

##
``

#### 问题描述：

```
Example 
```


#### Solutions：

#### Codes:


##
``

#### 问题描述：

```
Example 
```


#### Solutions：

#### Codes:
