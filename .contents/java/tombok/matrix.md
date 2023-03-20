- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Mátrix

- többdimenziós tömb
- sorindex és oszlopindex i és j
- 2 ciklus kell a bejáráshoz
- első a sorindex: i
- második az oszlopindex: j

```
//3X4 mátrix: 3 sor és 4 oszlop
int[][] matrix = {
	{1,44,66,88},
	{77,49,93,11},
	{2,52,17,5}
};

System.out.println(matrix[2][1]); //52
System.out.println(matrix[1][3]); //11
```

- mátrix elemeinek kiírása formázottan tabluátorral határolva
- külső forciklus lépteti a sorokat, a belső az oszlopelemeket

```
System.out.println("Mátrix elemei: ");
for (int i = 0; i < matrix.length; i++) {
	for (int j = 0; j < matrix[i].length; j++) {
		System.out.print(matrix[i][j] + "\t");
	}
	System.out.println();
}
System.out.println();
System.out.println();
```

- Feladat02: 5X6-os mátrix feltöltése (sorszintű) véletlen számokkal 1-100 között 
- mátrix elemeit formázottan tabulátorral írjuk ki!

```
int[][] matrix2 = new int[5][6];
Random r = new Random();
		
/* mátrix elemeinek feltöltése */
for (int i = 0; i < matrix2.length; i++) {
	for (int j = 0; j < matrix2[i].length; j++) {
		matrix2[i][j] = r.nextInt(100)+1;
	}
}

/* mátrix elemei */
System.out.println("Mátrix2 elemei: ");
for (int i = 0; i < matrix2.length; i++) {
	for (int j = 0; j < matrix2[i].length; j++) {
		System.out.print(matrix2[i][j] + "\t");
	}
	System.out.println();
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
