- két halmaz elemei közül legalább az egyikben szerepelnie kell.
- A halmazokon belül nincs ismétlődés

```
private static boolean decide(int[] arr, int search) {
	boolean itsIn = false;
	int i = 0;

	do {
		if (arr[i] == search) {
			itsIn = true;
		}
		i++;
	} while (!itsIn && i < arr.length);
	return itsIn;
}

private static int matchesNumbersDefines(int[] arrA, int[] arrB) {
	int count = 0;

	for (int i = 0; i < arrB.length; i++) {
		if (decide(arrA, arrB[i])) {
			count++;
		}
	}
	return count;
}

private static int[] resultArray(int[] arrA, int[] arrB) {
	int arraySize = (arrA.length + arrB.length) - matchesNumbersDefines(arrA, arrB);
	int[] resultArray = new int[arraySize];

	//1.lépés arrA-ból minden elemet belepakolok az eredmenytömbbe
	for(int i = 0; i < arrA.length; i++) {
		resultArray[i] = arrA[i];
	}

	//2. lépés: arrB-ből azokat helyezzük bele, ami még nincs benne
	int resultArraySize = arrA.length;

	for(int i = 0; i < arrB.length; i++) {
		if(!decide(resultArray, arrB[i])) {
			resultArray[resultArraySize] = arrB[i];
			resultArraySize++;
		}
	}
	return resultArray;		
}

public static void main(String[] args) {
	int[] arrA = {1,2,3,4,5,6,7,8,9,10};
	int[] arrB = {6,7,8,9,10,11,12,13,14,15};

	System.out.print("\"A\" tömb elemei: ");
	for(int item : arrA) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("\"B\" tömb elemei: ");
	for(int item : arrB) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Unio: ");
	for(int item : resultArray(arrA, arrB)) {
		System.out.print(item + " ");
	}
}
```
