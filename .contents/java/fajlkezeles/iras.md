- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Írás

```
public static void main(String[] args) {
```

- a második paraméter append kapcsoló, ha igaz,
- akkor hozzáírja a meglévő tartalomhoz

```
		try {
			FileWriter fw = new FileWriter("gumiKacsa/kimenet.txt", false);
			fw.write("alma...\r\n");
			fw.write("körte...\r\n");
			
			int[] tomb = {99,1,14,2};
			
			for (int item : tomb) {
				fw.write(String.valueOf(item));
				fw.write("\r\n");
			}
```

> nagyon fontos a lezárás, ha kimarad létrehozza, de nem ír bele semmit

```
			fw.close();
			System.out.println("Elkészült a fájl!!!");
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
