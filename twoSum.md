**Problem**: https://leetcode.com/problems/two-sum/
#Solution

```javascript

/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
	let result = [];
    for (let i = 0; i < nums.length; i++) {
    	for (let j = i+1; j < nums.length; j++) {
    		if (nums[i]+nums[j]==target) {
    			result[result.length]=i;
    			result[result.length]=j;
    		}
    		
    	}
    }
    return result;
};


//test case
var result = twoSum(nums=[2, 7, 11, 15],target=9);
console.log(result);

```

The whole basci idea is use two loop to get all the combination.That means:

We first add the element 1 and the other element begins by 2,3,4....n

Then we adjust to the second round, add the element 2 and other element begins by 3,4,5....n

The complexity is (n*(1+(n-1)))/2 => O(n^2), it is not so efficient. 
