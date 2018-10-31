You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Example:

Input: (2 -> 4 -> 3) + (5 -> 6 -> 4)
Output: 7 -> 0 -> 8
Explanation: 342 + 465 = 807.








`思路`

本题主要是类似数据在机器中存储的方式，我们平常所见的数据比如342，
在链表中是逆向存储的所以就成了2->4->3这样了，同样5 -> 6 -> 4就是465，
如果这样转换后，我们就会发现342+465=807，在十位上相加是超过10向前进一，
但是链表是逆向的，所以就是向后进一。 
因此，本题可以把链表中的元素转换为相应的数据后进行相加，得到的结果在按照相应的格式放入链表中。
也可以直接按照链表的方式进行相加，在相加的过程中判断其是否要进位，如果需要进位是向后进位的。


`官方解法`

根据官方solution的方法，可以采用一个进位carry方便的完成一次遍历得出结果，不过过程稍微麻烦。

![add_two_nums](https://github.com/hanlaoshi/leetcode-DailyProblem/blob/master/img-storage/add_two_nums.png?raw=true)

两个要注意的地方：如果列表长度不相等；如果列表相加完成最后仍有进位位。
