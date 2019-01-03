## 判断是否有重复元素
    给定一个整数数组，判断是否存在重复元素。
    如果任何值在数组中出现至少两次，函数返回 true。如果数组中每个元素都不相同，则返回 false。
#### 示例1
    输入: [1,2,3,1]
    输出: true
#### 示例2
    输入: [1,2,3,4]
    输出: false
#### 示例3
    输入: [1,1,1,3,3,4,3,2,4,2]
    输出: true
### 思路
    1 首先判断当数组为空或者只有一个元素时，自然时返回false
    2 创建一个数组并去重
    3 比较新数组和原数组的长度  
### 答案  
```  javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var removeDuplicates = function(nums) {
    if(nums.length == 0 || nums.length == 1) return false  // 当数组为空活着只有一个元素，则返回false
    var arr =[...new Set(nums)];// 数组去重。返回新数组
    if(arr.length == nums.length){
        return false
    }else{
        return true
    }
};
```