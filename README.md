# dsa8
#Dutch national flag algorithm
#Sort an array of 0s, 1s and 2s 
#efficient solution
#java_code
 int a[]={0,1,1,0,1,2,1,2,0,0,0,1};
        int low=0;
        int mid=0;
        int high=a.length-1;
        int temp;
        while(mid<=high)
        {
            if(a[mid]==0)
            {
               temp=a[mid];
               a[mid]=a[low];
               a[low]=temp;
               mid++;
               low++;
            }
            else if(a[mid]==1)
            {
                mid++;
            }
            else if(a[mid]==2)
            {
                temp=a[mid];
                a[mid]=a[high];
                a[high]=temp;
                high--;
            }
        }
