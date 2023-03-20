```
public static void main(String[] args) {
		
	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("A tömb rendezve: ");
	minChangeSort(arr);
}

private static void minChangeSort(int[] arr) {
	int change;
	int minIndex;

	for (int i = 0; i < arr.length; i++) {
		minIndex = i;
		for (int j = i+1; j < arr.length; j++) {
			if (arr[j] < arr[minIndex]) {
				minIndex = j;
			}
		}
	
		//csere
		if (i != minIndex) {
			change = arr[i];
			arr[i] = arr[minIndex];
			arr[minIndex] = change;
		}
		System.out.print((i+1) + ".futás: ");
		for(int item : arr) {
			System.out.print(item + " ");
		}
		System.out.println();
	}
}
```
