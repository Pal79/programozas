---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---

# Ciklusok

- Ciklust mikor használunk?
- Ha ismétlődő utasításra vagy utasításokra van szükség
- For ciklust mikor használjuk?
- Tudjuk, hogy hányszor kell ismételni.

- Példákban: ismételd 5X, valahányszor,
- tömbkezelő műveletek,
- intervallumon belüli vizsgálat

- Feladat01: Bekérjuk a felhasználó nevét, majd kiírjuk ötször

```
System.out.println("Feladat1 - Név 5X:");

System.out.print("Kérem adja meg a nevét: ");
String nev = sc.nextLine();

// for (int i = 0; i < ismetlesSzam; i++) {}

for (int i = 0; i < 5; i++) {
	/* ciklusmag: annyiszor kerül végrehajtásra, ahányszor a ciklus */
	System.out.println((i+1) + ".futás: " + nev);
}
System.out.println();
```
		
- Feladat02: Kérjünk be egy szöveget és ismétlésszámot,
- majd írjuk ki egymás alá a szöveget annyiszor,
- amekkora értéket megadtunk!

```
System.out.println("Feladat02: szöveg valahányszor: ");
System.out.print("Kérem adja meg a szöveget: ");
String szoveg = sc.nextLine();

System.out.print("Adjon meg egy ismétlésszámot: ");
int ismetlesSzam = Integer.parseInt(sc.nextLine());

for (int i = 0; i < ismetlesSzam; i++) {
	System.out.println(szoveg);
}
System.out.println();
```

- Feladat03: Kérjünk be 5 egész számot,
- majd mindegyikről döntsük el,
- hogy osztható-e hárommal maradék nélkül!

```
System.out.println("Feladat03: Osztható -e hárommal:");

int szamBekert; //deklaráció

for (int i = 0; i < 5; i++) {
	System.out.print("Kérem adja meg a(z): " + (i+1) + "/5 számot: ");
	szamBekert = Integer.parseInt(sc.nextLine()); //definíció

	if (szamBekert % 3 == 0) {
		System.out.println("Hárommal osztható");
	} else {
		System.out.println("Nem osztható hárommal");
	}
}		
System.out.println();
```

- Feladat04: 10-től visszafelé 1-ig egyessével,
- szóközzel elválasztva egymás mellé írjuk ki a számokat

```
System.out.println("Feladat4: 10-től 1-ig számok egyessével");

for (int i = 10; i > 0; i--) {
	System.out.print(i + " ");
}		
System.out.println();
```

- Feladat05: Kérjünk be egy kezdő és egy végértéket,
- majd írjuk ki a két érték közötti hárommal és néggyel
- maradék nélkül osztható számokat (egymás mellé szóközzel elválasztva)

```
System.out.println("Feladat05: intervallumvizsgálat");

System.out.print("Kérem adja meg a kezdőértéket: ");
int kezdoErtek = Integer.parseInt(sc.nextLine());

System.out.print("Kérem adja meg a végértéket: ");
int vegErtek = Integer.parseInt(sc.nextLine());

for (int i = kezdoErtek; i <= vegErtek; i++) {
	if (i % 3 == 0 && i % 4 == 0) {
		System.out.print( i + " ");
	}
}
```
		
### While ciklus

- Mikor használjuk?
- Mikor nem tudjuk, hogy hányszor fut le.
 
- Elöltesztelős ciklus:
   - először megnézi a ciklusfeltételt, ha igaz,
   - akkor lefuttatja azt, amit a ciklusmagban talál.
   - Lehet, hogy egyszer sem fut le.

- Végtelen ciklus:
   - Nem ér véget, nem áll le.
   - Mi okozza?
   - Ha rosszul határozzuk meg a kilépési feltételt.

- Feladatoknál kulcsszó:
   - fájlkezelés: amíg a fájl végéig nem érünk
   - NAGYON fontos a ciklusfeltétel helyes megfogalmazása, hogy ne legyen végtelen ciklus.

- Feladat: Vegyünk számokat 0-tól,
- addig amig a 7-tel osztható számok összege át nem lépi a 100-at!

```
int szamlalo = 0;
int osszeg = 0;

while (osszeg < 100) {
	//ciklusmag
	szamlalo++;

	if (szamlalo%7 == 0) {
		osszeg += szamlalo; //osszeg = osszeg + szamlalo;
		System.out.println(szamlalo);
	}
}

System.out.println("Számláló értéke: " + szamlalo);
System.out.println("Összeg értéke: " + osszeg);
```

### Do-While ciklus

- Itt sem tudjuk, hogy hányszor kell ismételni
- hátultesztelős ciklus
- egyszer biztosan lefut, utána ellenőrzi a feltételt,
- ha igaz, akkor belemegy a ciklusba és végrehajta, amit a ciklusmagban talál

- Feladat1: Addig kérek be számokat, amíg 0-at nem adok meg!

```
System.out.println("Feladat01: Számok, amíg nem 0:");

// szamBekert változónál a dek. és def. szétszedjuk, azért, hogy a feltötesnél lássa a ciklus

do {
	System.out.print("Adjon meg egy egész számot (0-ra kilép): ");
	szamBekert = Integer.parseInt(sc.nextLine());
} while (szamBekert !=0);

System.out.println("Kiléptem, mert 0-at adtál meg...");
```

- Feladat02: Addig dobok 6oldalú kockával, amíg 6-os nem lesz

```
System.out.println("Feladat02: kockadobós 6-osig");
Random r = new Random();
int velSzam;

do {
	velSzam = r.nextInt(6)+1;
	System.out.print(velSzam + " ");
} while (velSzam !=6);
System.out.println();
System.out.println("6-ost dobtál gratulálok!!!");
```

---

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
