- Egy halmazon belül keressük a legkisebb értékű elemet

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	int min = arr[0];
	int minIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] < min) {
			min = arr[i];
			minIndex = i;
		}
	}
	System.out.println("Minimum érték a tömbben: " + min + "\nMinimum érték indexe: " + minIndex);
}
```
