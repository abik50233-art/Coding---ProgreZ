#include <vector>
#include <unordered_map>

using namespace std;

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> numMap; // Stores {value, index}
        
        for (int i = 0; i < nums.size(); i++) {
            int complement = target - nums[i];
            
            // Check if the complement is already in the map
            if (numMap.find(complement) != numMap.end()) {
                return {numMap[complement], i};
            }
            
            // If not found, add current number and its index to the map
            numMap[nums[i]] = i;
        }
        
        // Since the problem guarantees one solution, we don't need a fallback
        return {};
    }
};
