- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Maximum kiválasztás

- egy halmazon belül keressük
- a legnagyobb értékű elemet.

- kiegészítés: Melyik indexen van a legnagyobb érték?

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	int max = arr[0];
	int maxIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] > max) {
			max = arr[i];
			maxIndex = i;
		}
	}
	System.out.println("Maximum érték a tömbben: " + max + "\nMaximum érték indexe: " + maxIndex);
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
