- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Tömb

- összetett adattípus,
- több azonos típusú érték tárolására alkalmas,
- az elemeket a tömb nevével és indexével íratjuk ki.

- Fontos kötöttség: meg kell adnunk, hogy milyen típusokat tárol és
- létrehozáskor meg kell adni a méretét is (vagy az egyes elemeket)
- az indexelés 0-tól indul
- Egy dimenziós tömb - vektor

```
int[] tomb = {3,6,77,22,98};

System.out.println(tomb[2]);//77
System.out.println(tomb[3]);//22

tomb[2] = 43;
System.out.println(tomb[2]); //43
```

> tömbméret lekérdezés

```
System.out.println("A tömb mérete: " + tomb.length);
```

> utolsó elem kiírása

```
System.out.println("Az utolsó elem: " + tomb[tomb.length-1]);
//System.out.println("Az utolsó elem másként: " + tomb[5]);
//ArrayIndexOutOfBoundsException
//System.out.println("Az utolsó elem másként: " + tomb[4]);

System.out.println();		
//System.out.println(tomb); // [I@7852e922
```

> tömbbejárás - For ciklussal

```
System.out.println("A tömb elemei: ");
	for (int i = 0; i < tomb.length; i++) {
	System.out.print(tomb[i] + " ");
}
System.out.println();
```

- tömbbejárás - Foreach szerkezettel
- ha nem fontos az indexelés, akkor bejárhatjuk ezzel is
- Vegyél minden egyes elemet egymás után a tömbön belül

```
System.out.println("A tömb bejárása FOREACH szerkezettel: ");
for (int item : tomb) {
	System.out.print(item + " ");
}
System.out.println();
```

> String tömb deklarációja és definiciója

```
String[] nevek = {"Elek", "János", "Tamás"};
System.out.println(nevek[2]); //Tamás
//System.out.println(nevek[3]); //ArrayIndexOutOfBoundsException

char[] karakterek = {'g','r','w'};
System.out.println(karakterek[1]); //r
```

- Feladat01: Töltsünk fel egy 20 elemű tömböt véletlen számokkal 1-100
   - között, majd írjuk ki a tömb elemeit egymás mellé!

```
int[] tombVeletlen = new int[20]; // üres 20 elemű tömb deklaráció:
//20*4byte - new kulcszó memória foglalás

System.out.println(tombVeletlen[0]); // első elem a tömbön belül: 0
System.out.println("Tömb elemei 0-val:");

for (int item : tombVeletlen) {
	System.out.print(item + " ");
}
System.out.println();
System.out.println();

Random r = new Random();

for (int i = 0; i < tombVeletlen.length; i++) {
	tombVeletlen[i] = r.nextInt(100)+1;
}
```

> tombkiírás - Foreach szerkezettel

```
System.out.print("A véletlen tömb elemei: ");
for (int item : tombVeletlen) {
	System.out.print(item + " ");
}
System.out.println();
System.out.println();
```

> Feladat02: 5 elemű tömb feltöltése a felhasználótól érkező egész számokkal

```
Scanner sc = new Scanner(System.in);
int[] tomb2 = new int[5];
for (int i = 0; i < tomb2.length; i++) {
	System.out.print("Adja meg a " + (i+1) + "/5 elemet: ");
	tomb2[i] = Integer.parseInt(sc.nextLine());
}

System.out.print("Tomb2 elemei: ");
for (int item : tomb2) {
	System.out.print(item + " ");
}

sc.close();
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
