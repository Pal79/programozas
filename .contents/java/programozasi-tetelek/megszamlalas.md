- Meghatározza egy halmazon belül az adott tulajdonságú elemek számát

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	int evenCount = 0;
	int unmatchedCount = 0;

	for(int item : arr) {
		if(item % 2 == 0) {
			evenCount++;
		} else {
			unmatchedCount++;
		}
	}
	System.out.println("A tömb páros elemeinek száma: " + evenCount + "\nA tömb páratlan elemeinek száma: " + unmatchedCount);
}
```
