#include <vector>
#include <string>

using namespace std;

class Solution {
public:
    vector<string> letterCombinations(string digits) {
        if (digits.empty()) return {};

        // Mapping of digits 2-9 to letters
        vector<string> phoneMap = {
            "abc",  // 2
            "def",  // 3
            "ghi",  // 4
            "jkl",  // 5
            "mno",  // 6
            "pqrs", // 7
            "tuv",  // 8
            "wxyz"  // 9
        };

        vector<string> result;
        string current;
        backtrack(digits, 0, phoneMap, current, result);
        return result;
    }

private:
    void backtrack(const string& digits, int index, const vector<string>& phoneMap, 
                   string& current, vector<string>& result) {
        // Base case: if we've processed all digits, add current combination to results
        if (index == digits.length()) {
            result.push_back(current);
            return;
        }

        // Get letters corresponding to the current digit
        string letters = phoneMap[digits[index] - '2'];
        for (char letter : letters) {
            current.push_back(letter);       // Choose
            backtrack(digits, index + 1, phoneMap, current, result); // Explore
            current.pop_back();              // Un-choose (Backtrack)
        }
    }
};
