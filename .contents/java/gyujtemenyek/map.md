- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Map Interface

```
public static void main(String[] args) {
```

> Map interface: kulcs-érték párokat tartalmazó adatszerkezet

- Tulajdonságai:
   - kulcsnak egyedinek kell lennie
   - Rendezett formája a SortedMap

- Map interface-t megvalósító (implementáló) osztályok:
   - HashMap, LinkedHashMap

- Mi a különbség a Hashtable és HashMap között?
   - Hashtable -> java 1.7 óta elavult (deprecated)
   - Hashtable -> többszálú feldolgozás (szálbiztos)
   - HashMap -> nem szálbiztos, többszálú feldolgozásra nem alkalmas, helyette alkalmazható syncronizedMap vagy concurrentHashMap
   - HashMap -> implentálja az iterable interface - for ciklussal bejárható
   - Hashtable -> Enumeration interface-t implementálja

- Konkluzió: HashMap-et használjunk kulcs-értékpárok tárolására, tóbbszálúnál:
   - syncronizedMap vagy concurrentHashMap

- Az adatszerket kulcs alapján való keresésre van optimalizálva!

```
	Map<String, Integer> gyumolcsArak = new HashMap<String, Integer>();
	gyumolcsArak.put("alma", 750);
	gyumolcsArak.put("szilva", 350);
	gyumolcsArak.put("barack", 980);
	System.out.println(gyumolcsArak);

	gyumolcsArak.put("alma", 760);
	System.out.println(gyumolcsArak); //760 lett az ára az almának
```

> HashMap bejárása - foreach

```
	for (Map.Entry<String, Integer> item : gyumolcsArak.entrySet()) {
		System.out.println("Kulcs=" + item.getKey() + ", érték: " + item.getValue());
	}	
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
