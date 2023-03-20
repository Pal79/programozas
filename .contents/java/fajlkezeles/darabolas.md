- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Darabolás

```
String fileName = "gumiKacsa/adatokDarabol.txt";
Path fileNamePath = Paths.get(fileName);

try {
	BufferedReader br = new BufferedReader(new InputStreamReader(new FileInputStream(fileName), "UTF-8"));
```

> 1. lépés: derítsük ki hány soros a fájl

```
	long lineCount = Files.lines(fileNamePath).count();

	//System.out.println("Sorok száma: "+lineCount);
```

> tömbméretnél csak integer típus szerepelhet

```
	int arraySize = (int)lineCount;
	String[] names = new String[arraySize];
	int[] heights = new int[arraySize];

	for (int i = 0; i < arraySize; i++) {
```

> 1. lépés: Beolvasunk egy sort

```
		String sor = br.readLine();
```

> 2. lépés határoló mentén (;) szétdaraboljuk a sort - split
   >0-as indexre kerül a név, 1-re a magasság

```
		String[] sorAdatok = sor.split(";");
		//System.out.println(sorAdatok[0] + " - "+sorAdatok[1]);
		names[i] = sorAdatok[0];
		heights[i] = Integer.parseInt(sorAdatok[1]);
	}
	br.close();

	for (int i = 0; i < heights.length; i++) {
		System.out.println("Név: " + names[i] + ", magasság: " + heights[i] + "cm");
	}
```

> Feladat: Ki a legmagasabb? Válaszban a név és magasság is jelenjen meg!

```
	int max = heights[0];
	int maxIndex = 0;
	for (int i = 0; i < heights.length; i++) {
		if (heights[i]>max) {
			max = heights[i];
			maxIndex = i;
		}
	}
	System.out.println("Legmagasabb ember: " + names[maxIndex] + ", magasság: "+heights[maxIndex] + "cm");

} catch (UnsupportedEncodingException e) {
	// TODO Auto-generated catch block
	e.printStackTrace();
} catch (FileNotFoundException e) {
	// TODO Auto-generated catch block
	//e.printStackTrace();
	System.out.println("Nem találom a fájlt!!!");
} catch (IOException e) {
	// TODO Auto-generated catch block
	e.printStackTrace();
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
