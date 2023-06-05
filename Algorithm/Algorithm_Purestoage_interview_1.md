# Find double
Please refer the Algorithm_Purestoage_interview_1.png in the same folder.

The optimal solution is using int array. Note: The number won't be larger than 1000, but the length of list could be 100000, so counting from [0, 1000] is much faster than sorting on 100000 with O(nlgn).

1.declare an int array
2.count frequency by iterating the list with the int array
3.for each number i, check counter[i] and counter[i * 2] == 1, then append i * counter[i] to the result list
4.return list or print out.
