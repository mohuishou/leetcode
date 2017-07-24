# 1. TwoSum

## js

```javascript
var twoSum = function(nums, target) {
    let o={}
    for(let i=0;i<nums.length;i++){
        o[nums[i]]=i
    }
    for(let i=0;i<nums.length;i++){
        let tmp = target - nums[i]
        if (tmp in o && o[tmp] != i){
            return i > o[tmp] ? [o[tmp],i] : [i,o[tmp]]
        }
    }
    return false
};
```

## go
