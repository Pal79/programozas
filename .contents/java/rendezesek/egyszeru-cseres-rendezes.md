```
public static void main(String[] args) {

	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Tömb elemei rendezve: ");
	for(int item : exchangeSort(arr)) {
		System.out.print(item + " ");
	}
}

private static int[] exchangeSort(int[] arr) {
	for(int i = 0; i < arr.length-1; i++) {
		for(int j = i+1; j < arr.length; j++) {
			if(arr[i] > arr[j]) {
				int temp = arr[j];
				arr[j] = arr[i];
				arr[i] = temp;
			}
		}
	}

	return arr;
}
```
