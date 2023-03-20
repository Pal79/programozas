- azoknak az elemeknek a kiválasztása,
- amelyek mind a két halmazban megtalálhatóak.

- Az egyes tömbökön belül nem lehetnek ismétlődések.

```
public static boolean decide(int[] arr, int search) {
	boolean itsIn = false;
	int i = 0;

	do {
		if(arr[i] == search) {
			itsIn = true;
		}
		i++;
	} while(!itsIn && i < arr.length);

	return itsIn;
}

public static int newArraySize(int[] arrA, int[] arrB) {
	// kiderítjük, hány darab egyezés van - ez lesz az új tömb mérete
	int count = 0;

	for(int i = 0; i < arrB.length; i++) {
		if(decide(arrA, arrB[i])) {
			count++;
		}
	}

	return count;
}

public static int[] resultArrListening(int[] arrA, int[] arrB) {
	int[] resultArr = new int[newArraySize(arrA, arrB)];
	int index = 0;

	for(int i = 0; i < arrB.length; i++) {
		if(decide(arrA, arrB[i])) {
			resultArr[index] = arrB[i];
			index++;
		}
	}
	return resultArr;
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

	System.out.print("Metszet: ");
	for(int item : resultArrListening(arrA, arrB)) {
		System.out.print(item + " ");
	}
}
```
