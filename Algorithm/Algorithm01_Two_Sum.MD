# 1. Two Sum
https://leetcode.com/problems/two-sum/
I like this problem, as it introduces many cases, and it doesn't use complicated algorithm, which is suitable for interview.

c++:
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

Python3:
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        my_dict = {}

        for index in range(len(nums)):
            item = target - nums[index]

            if nums[index] in my_dict:
                return [index,  my_dict[nums[index]]]
            else:
                my_dict[item] = index

        return []

