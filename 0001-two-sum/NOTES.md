# Notes for 0001 - Two Sum

### Key Concepts:
- Arrays in Java must be created using the `new` keyword, since they are objects.
- Always handle edge cases and return fallback responses (e.g., an empty array).
- A brute-force solution has O(n²) time complexity, but we can improve this using a HashMap.

---

### Optimized Solution Using HashMap (O(n) Time)

```java
import java.util.HashMap;

class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            if (map.containsKey(complement)) {
                return new int[]{map.get(complement), i};
            }
            map.put(nums[i], i);
        }
        return new int[]{}; // fallback
    }
}
``
