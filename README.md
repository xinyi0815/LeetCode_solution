# LeetCode_solution
//1929. Concatenation of Array
/**
 * Note: The returned array must be malloced, assume caller calls free().
**/

int* getConcatenation(int* nums, int numsSize, int* returnSize){
    int *a;
    a = (int*)malloc(sizeof(int) * numsSize * 2);
    for(int i = 0; i < numsSize; i++)
        a[i] = nums[i];
    int j = 0;
    for(int i = numsSize; i < 2 * numsSize; i++)
    {
        a[i] = nums[j];
        j++;
    }
    *returnSize = numsSize * 2;
    return a;
}
