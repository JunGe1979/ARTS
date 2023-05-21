# 24. Swap Nodes in Pairs
https://leetcode.com/problems/swap-nodes-in-pairs/description/
I like this problem, as it introduces many cases, and it doesn't use complicated algorithm, which is suitable for interview.

class Solution {
public:
	ListNode* swapPairs(ListNode* p1) {
		if (p1 == NULL)
			return NULL;

		ListNode * result = (p1->next ? p1->next : p1);
		while (p1) {
			ListNode * p2 = p1->next;
			ListNode * p3 = (p2 ? p2->next : NULL);

			if (p2)
				p2->next = p1;

			if (p3 == NULL)
				p1->next = NULL;
			else
				p1->next = (p3->next ? p3->next : p3);

			p1 = p3;
		}
		return result;
	}
};
