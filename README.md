## Leetcode_practice
Toady, my leetcode career is start.

## 1 Two Sum
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

## 2 Add Two Numbers
```
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode p1=l1;
        ListNode p2=l2;
        ListNode dummy=new ListNode(0);
        ListNode p=dummy;
        int jinwei=0;
        
        while(p1 != null| p2 != null){
            int val=jinwei;
            if(p1!=null){
                val+=p1.val;
                p1=p1.next;
            }
            if(p2!=null){
                val+=p2.val;
                p2=p2.next;
            }
            jinwei=jinwei/10;
            val=val%10;
            p.next = new ListNode(val);
            p = p.next;
        }
        return dummy.next;
    }
}
//时间复杂度 ，空间复杂度 
```
## 104 Maximum Depth of Binary Tree
```
class Solution {
    public int maxDepth(TreeNode root) {
        if(root == null){
            return 0;
        }
        int leftmax = maxDepth(root.left);
        int rightmax = maxDepth(root.right);
        int res = Math.max(leftmax , rightmax);
        res = res + 1;
        return res;
    }
}
//时间复杂度 O(N)，空间复杂度 O(logN)
```
## 144 Binary Tree Preorder Traversal
```
class Solution {
    List <Integer> res = new LinkedList<>();
    public List<Integer> preorderTraversal(TreeNode root) {
        transerve(root);
        return res;
    }
    void transerve(TreeNode root){
        if(root == null){
            return ;
        }
        res.add(root.val);
        transerve(root.left);
        transerve(root.right);
    }
}
//时间复杂度 O()，空间复杂度 O()
```
