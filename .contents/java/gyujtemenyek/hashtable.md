- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# HashTable

```
public static void main(String[] args) {
```

> kulcs értékpárokban történik az adattárolás

```
	Hashtable<String, String> szotar = new Hashtable<>();
	szotar.put("apple", "alma");
	szotar.put("pear", "körte");
	szotar.put("banana", "banán");

	//szotar.clear(); //kitörli a teljes tartalmát

	szotar.remove("apple");

	System.out.println("Van-e apple kulcsunk: " + szotar.containsKey("apple"));
	System.out.println("Van-e pear kulcsunk: " + szotar.containsKey("pear"));
```

>  kulcsnak egyedinek kell lennie és csak 1X szerepelhet

```
	szotar.put("pear", "korte");
	System.out.println(szotar);
	szotar.put("pear2", "korte");
	System.out.println(szotar);
```

- Hashtable bejárása
- For ciklus és foreach nem használható bejárásra,
- mert a Hashtable nem implementálja az iterable interface-t

> Enumeration interface-t implementálja a Hashtable */

```
	Enumeration<String> enumeration = szotar.keys();

	while (enumeration.hasMoreElements()) {
		String kulcs = enumeration.nextElement();
		System.out.println("Angol: " + kulcs + "\t Magyarul: " + szotar.get(kulcs));
	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
