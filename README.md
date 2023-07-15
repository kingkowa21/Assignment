import java.util.Arrays;
public class Assignment {
    public static void main(String[] args) {
    int arr[]={1,2,3,4,5};
    int r=2;
    rotate(arr,r);
    System.out.println(Arrays.toString(arr));
    }
    public static void rotate(int[] arr, int Count) {
        if (arr == null || arr.length == 0 || Count <= 0) {
            return;
        }
        int length = arr.length;
        Count = Count % length;
        reverse(arr, 0, length - 1);
        reverse(arr, 0, Count - 1);
        reverse(arr, Count, length - 1);
    }
    private static void reverse(int[] arr, int start, int end) {
        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }

}
