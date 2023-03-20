- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Set Interface

```
public static void main(String[] args) {
```

- Halmazelméleti fogalmak szükségesek

- Set interface: speciális collection: nem tartalmazhat azonos elemket.
- A duplikáció kiszűrésére equals és hashcode metódusokat használ.

- Három implementációja van:

- HashSet: az elemeket táblákban tárolja és fontos az elemek bejárása
- TreeSet: gyors a bejárás, az elemeket fa adatszerkezetben tárolja, nehézkes a beszúrás, rendezetten tárolja az adatokat
- LinkedHashSet: láncolt lista és a Hashtábla tulajdonságait ötvözi

```
	int[] szamoktomb = {34,22,10,60,30,22};

	Set<Integer> setElemek = new HashSet<Integer>();
	for (int i = 0; i < szamoktomb.length; i++) {
		setElemek.add(szamoktomb[i]);
	}

	System.out.println(setElemek); //22-es csak 1X szerepel benne

	TreeSet<Integer> rendezettElemek = new TreeSet<Integer>(setElemek);
	System.out.println(rendezettElemek);

	System.out.println("Első elem (legkisebb érték): " + rendezettElemek.first());
	System.out.println("Utolsó elem (legnagyobb érték): " + rendezettElemek.last());
}
```

- Halmazműveletek - metódusok

- Két halmaz -> s1 és s2
   - s1.containsAll(s2) - részhalmaza s2 az s1
   - s1.addAll(s2) - az s1-be belekerül a két halmaz uniója
   - s1.retainAll(s2) - az s1-be belekerül a két halmaz metszete
   - s1.removeAll(s2) - az s1-be belekerül a két halmaz különbsége

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
