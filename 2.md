# 2. Add Two Numbers

## js

```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val) {
 *     this.val = val;
 *     this.next = null;
 * }
 */
/**
 * @param {ListNode} l1
 * @param {ListNode} l2
 * @return {ListNode}
 */
var addTwoNumbers = function(l1, l2) {
    let sum = 0;
    let l3 , p;
    while(l1!==null || l2!==null){
        if(l1!==null){
            sum=sum+l1.val;
            l1=l1.next;
        }
        if(l2!==null){
            sum=sum+l2.val;
            l2=l2.next;
        }
        if (!l3){
            l3 = new ListNode(sum % 10);
            p= l3;
        }else{
            p.next = new ListNode(sum % 10);
            p = p.next;
        }
        sum = sum > 9 ? 1 : 0;
    }
    if (sum == 1){
        p.next = new ListNode(1);
    }
    return l3;
};
```
