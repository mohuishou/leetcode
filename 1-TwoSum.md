# 1. TwoSum

## js

```javascript
function twoSum(nums,target){
    let o={}
    for(let i=0;i<nums.length;i++){
        o[nums[i]]=i
    }
    for(let x in o){
        let tmp = target - x
        if (tmp in o){
            return o[x] > o[tmp] ? [o[tmp],o[x]] : [o[x],o[tmp]]
        }
    }
    return false
}
```

## go
