## Leetcode_practice
Toady, my leetcode career is start.

## Two Sum
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i=0;i<nums.length;i++){
            for(int j=i+1;j<nums.length;j++){
                if(nums[j] == target - nums[i])
                    return new int[] {i,j};
            }
        }
        return new int[] {-1,-1};
    }
}
//时间复杂度 O(N^2)，空间复杂度 O(1)
```
