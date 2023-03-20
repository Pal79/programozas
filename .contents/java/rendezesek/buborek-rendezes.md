- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Buborék rendezés

```
public static void main(String[] args) {

	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Rendezett tömb elemei: ");
	for(int item : bubbleSort(arr)) {
		System.out.print(item + " ");
	}
}

public static int[] bubbleSort(int[] arr) {
	int temp;

	for(int i = 0; i < arr.length; i++) {
		for(int j = 0; j < arr.length-i-1; j++) {
			if(arr[j] > arr[j+1]) {
				temp = arr[j];
				arr[j] = arr[j+1];	
				arr[j+1] = temp;
			}
		}
	}
	return arr;
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
