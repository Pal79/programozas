- egy halmaz elemei közül kiválogatjuk
- az adott tulajdonságú elemket

```
public static int evenPieceCount(int[] arr) {
	int count = 0;
	for (int item : tomb) {
		if (item %2==0) {
			count++;
		}
	}
	return count;
}

public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	System.out.print("A tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	int[] evenArray = new int[evenPieceCount(arr)];
	int[] unmatchedArray = new int[arr.length - evenPieceCount(evenArray)];
	int evenIndex = 0;
	int unmatchedIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] % 2 == 0) {
			evenArray[evenIndex] = arr[i];
			evenIndex++;
		} else {
			unmatchedArray[unmatchedIndex] = arr[i];
			unmatchedIndex++;
		}
	}

	System.out.print("A tömb páros elemei: ");
	for(int item : evenArray) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("A tömb páratlan elemei: ");
	for(int item : unmatchedArray) {
		System.out.print(item + " ");
	}
}
```
