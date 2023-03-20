- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Kiválasztás

- egy sorozatban keresünk egy elemet,
- de biztosan tudjuk, hogy valahol benne van.

```
public static int selection(int[] arr, int search) {
	int i = 0;
	while (arr[i] != search) {
		i++;
	}
	return i;
}

public static void main(String[] args) {
	int index = 10;
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	System.out.println("A keresett szám indexe: " + selection(arr, index));
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
