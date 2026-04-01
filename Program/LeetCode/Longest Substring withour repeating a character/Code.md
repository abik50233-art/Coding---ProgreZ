#include <string>
#include <vector>
#include <algorithm>

using namespace std;

class Solution {
public:
    int lengthOfLongestSubstring(string s) {
        // Use an array as a hash map for ASCII characters (128 possible chars)
        // Stores the last seen index of each character
        vector<int> charIndex(128, -1);
        int maxLength = 0;
        int left = 0;

        for (int right = 0; right < s.length(); right++) {
            // If the character was seen before and is within the current window
            if (charIndex[s[right]] >= left) {
                left = charIndex[s[right]] + 1;
            }

            // Update the last seen position of the character
            charIndex[s[right]] = right;
            
            // Calculate window size and update max
            maxLength = max(maxLength, right - left + 1);
        }

        return maxLength;
    }
};
