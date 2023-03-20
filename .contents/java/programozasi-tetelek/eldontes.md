- egy halmazon belül vizsgáljuk,
- hogy egy érték benne van,
- vagy nincs.

- true/false

```
public static boolean decide(int[] arr, int search) {
	boolean answer = false;
	int i = 0;

	while (i < arr.length && arr[i] != search) {
		i++;
	}

	if (i < arr.length) {
		answer = true;
	}
	return answer;
}

public static void main(String[] args) {
	int search = 10;
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	if(decide(arr, search)) {
		System.out.println("Az adott szám: " + search + " benne van a tömbben.");
	} else {
		System.out.println("Az adott szám: " + search + " nincs benne a tömbben.");
	}
}
```
