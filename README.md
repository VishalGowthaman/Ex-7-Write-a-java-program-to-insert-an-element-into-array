# Ex-7 Write a java program to insert an element into array
# program
```
public class ArrayInsertion {
    public static void main(String[] args) {
        int[] originalArray = {1, 2, 3, 4, 5};
        int elementToInsert = 99;
        int indexToInsert = 2;

        int[] newArray = insertElement(originalArray, elementToInsert, indexToInsert);

        System.out.print("Original Array: ");
        for (int num : originalArray) {
            System.out.print(num + " ");
        }

        System.out.println();

        System.out.print("Array after insertion: ");
        for (int num : newArray) {
            System.out.print(num + " ");
        }
    }

    public static int[] insertElement(int[] arr, int element, int index) {
        int len = arr.length;
        int[] newArray = new int[len + 1];

        for (int i = 0; i < index; i++) {
            newArray[i] = arr[i];
        }

        newArray[index] = element;

        for (int i = index + 1; i <= len; i++) {
            newArray[i] = arr[i - 1];
        }

        return newArray;
    }
}

```
# output
![image](https://github.com/Rohith-AIDS/ARRAY/assets/94980736/41caf769-4e01-4854-bf52-114056d33f4f)
