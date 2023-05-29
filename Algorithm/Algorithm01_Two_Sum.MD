# 1. Two Sum
https://leetcode.com/problems/two-sum/
I like this problem, as it introduces many cases, and it doesn't use complicated algorithm, which is suitable for interview.

class Solution {
public:
	vector<int> twoSum(vector<int>& nums, int target)
	{
		map<int, int> dict;
		for (int i = 0; i<nums.size(); ++i)
		{
			if (dict.find(nums[i]) != dict.end())
			{
				return { dict[nums[i]], i };
			}
			else
			{
				dict[target - nums[i]] = i;
			}
		}

		return vector<int>();
	}
};
