# code1
int search(int nums[], int size, int target) 
{
    int left = 0;
    int right = size - 1;	
    while (left <= right) {	
        int middle = left + ((right - left) / 2);
        if (nums[middle] > target)
        {
            right = middle - 1;	
        }
        else if (nums[middle] < target) 
        {
            left = middle + 1;	
        }
        else {	
            return middle;
        }
    }
    return -1;
}
