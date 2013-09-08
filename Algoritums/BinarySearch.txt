/*
Binary search requires that the collection is already sorted. 
For example by Quicksort or Mergesort. 
Binary search checks the element in the middle of the collection. 
If the search element smaller or greater then the found element 
then a sub-array is defined which is then search again. 
If the searched element is smaller then the found element then the sub-array 
is from the start of the array until the found element. 
If the searched element is larger then the found element 
then the sub-array is from the found element until the end of the array.
 Once the searched element is found or the collection is empty then the search
  is over.
*/

public class BinarySearch {
  public static boolean contains(int[] a, int b) {
    if (a.length == 0) {
      return false;
    }
    int low = 0;
    int high = a.length-1;

    while(low <= high) {
      int middle = (low+high) /2; 
      if (b> a[middle]){
        low = middle +1;
      } else if (b< a[middle]){
        high = middle -1;
      } else { // The element has been found
        return true; 
      }
    }
    return false;
  }
} 