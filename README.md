# finding-missing-and-repeating-numbers-DSA
Brute to Optimal solution of Finding repeating and missing numbers. DSA question

So what can be the brute solution to this problem ?
Brute force - We will run a loop(say i) from 1 to N.
For each integer, i, we will count its occurrence in the given array using linear search.
We will store those two elements that have the occurrence of 2 and 0.
Finally, we will return the elements.
code -  public static int[] findMissingRepeatingNumbers(int[] a) {
        int n = a.length; // size of the array
        int repeating = -1, missing = -1;
        for(int i =1;i<n;i++){
        int cnt = 0 ;
        for(int j=0;j<n;j++){
         if(arr[j] == i) cnt++;
         }
         if(cnt == 2) repeating =i;
         if(cnt == 0) missing=i;
         if(repeating != -1 && missing != -1) break;
          }
        int[] ans = {repeating, missing};
        return ans;
    }
