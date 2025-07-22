Remember that array is to be created in java using "new" keyword as arrays are objects in java

Don't forget to return the edge case thingy as well. 

Using Hashmaps, we can get O(1) solution

import java.util.HashMap;

class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for(int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            if(map.containsKey(complement)) {
                return new int[]{map.get(complement), i};
            }
            map.put(nums[i], i);
        }
        return new int[]{}; // fallback
    }
}

HashMap<KeyType, ValueType> map = new HashMap<>();
A HashMap stores data in key-value pairs. Think of it like a dictionary:

Each key maps to a specific value.
Keys are unique.
Values can be duplicates.

Why Use a HashMap?

Fast lookup: O(1) average time for put() and get().
Perfect when you want to check if something exists or quickly retrieve a value by a key.
