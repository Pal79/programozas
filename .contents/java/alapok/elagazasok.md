- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Elágazások

- Mikor használjuk?
- Egy feltételtől függően a programunkat valamilyen irányba szeretnénk vezérelni.
- Három fajtája van: egyirányú, kétirányú és több irányú

### Egyirányú elágazás

##### csak az igaz ággal foglalkozunk

- Feladat01: Kérjük be a kinti hőmérsékletet,
- majd döntsük el,
- hogy fagy -e odakint (0 fok alatt van -e)!

```
System.out.println("Feladat - 1: Fagy -e? (egyirányú elágazás)");

System.out.print("Kérem adja meg a kinti hőmérsékletet(egész szám): ");
int homerseklet = Integer.parseInt(sc.nextLine());

/* a zárójelen belüli rész a feltétel (condition): úgy kell megfogalmazni,
 * hogy logikai tipus legyen true(igaz) vagy false(hamis)
 */

if (homerseklet < 0) {
	System.out.println("Fagy odakint!!!"); //Igaz blokk: ha a felt. igaz
}
System.out.println();
```

### Kétirányú elágazás

- Feladat02: Kérjünk be egy pozitív egész számot,
- majd döntsük el,
- hogy páros vagy páratlan!

```
System.out.println("2. feladat - páros - páratlan vizsgálat:");

System.out.print("Kérem adjon meg egy pozitív egész számot: ");
int egeszSzam = Integer.parseInt(sc.nextLine());

/* egyenlőség vizsgálatnál 2 db ==
 * TOP1 hiba feltételen belül vki. egy 1 db = -et rak!
 */

if (egeszSzam % 2 == 0) {
	//igaz ág
	//több utasítás is szerepelhet itt
	System.out.println("Páros...");
} else {
	//hamis ág
	//több utasítás is szerepelhet itt
	System.out.println("Páratlan");
}
System.out.println();
```

### Többirányú elágazás

> Mikor van rá szükség? Ha 2-nél több irány kell.

- Feladat03: Kérjünk be két egész számot,
- majd döntsük el,
- melyik kisebb/nagyobb esetleg egyenlő!

```
System.out.println("Feladat3: számok vizsgálata:");

System.out.print("Kérem adja meg az első számot: ");
int elsoSzam = Integer.parseInt(sc.nextLine());

System.out.print("Kérem adja meg a második számot: ");
int masodikSzam = Integer.parseInt(sc.nextLine());

/* else-if blokk akárhányszor ismétlődhet
 * if az eleje és else blokk a vége
 */

if (elsoSzam > masodikSzam) {
	System.out.println("Első szám nagyobb...");
} else if (masodikSzam > elsoSzam) {
	System.out.println("A második szám volt a nagyobb..");
} else {
	System.out.println("Egyenlő...");
} 
System.out.println();
System.out.println();
```

```
if (condition1) {
	implementation
} else if (condition2) {
	implementation
} else if (condition3) {
	implementation
} else {
	implementation
}
```

> pszeudó - mondatszerű leírás

```
ha (feltétel), akkor
	ut1
különben ha(feltétel2), akkor
	ut2
egyébként ut3
```
			
### Switch-case

> Többirányú elágazást valósít meg

> ez a szerkezet kötött a lehetőségek száma

> csak konkrét értéket tud vizsgálni (intervallumot nem)
		
- Feladat04: Bekérünk egy érdemjegyet számmal, majd kiírjuk szövegesen.

```
System.out.print("Kérem adja meg az érdemjegyet, egész szám(1-5): ");
int erdemJegy = Integer.parseInt(sc.nextLine());

switch (erdemJegy) {
	case 1: System.out.println("Elégtelen");
		break;
	case 2: System.out.println("Elégséges");
		break;
	case 3: System.out.println("Közepes");
		break;
	case 4: System.out.println("Jó");
		break;
	case 5: System.out.println("Jeles");
		break;
	default: System.out.println("Hibás értéket adott meg!!!");
		break;
}
System.out.println();
```

- default: alapértelmezett: ha egyik ágba sem megy bele
- break: a switch utáni részre ugrik- kilép a switch-ből
		
- Feladat: Bekérjuk a nap sorszámát,
- majd kiírjuk szövegesen,
- hogy hétköznap vagy hétvége esetleg hibás adat.

```
System.out.println("Feladat05: hétköznap/hétvége:");

System.out.println("Kérem adja meg a nap sorszámát, egész számmal(1-7): ");
int napSorSzam = Integer.parseInt(sc.nextLine());

switch (napSorSzam) {
	case 1:
	case 2:
	case 3: 
	case 4: 
	case 5: System.out.println("Hétköznap");
		break;
	case 6: 
	case 7: System.out.println("Hétvége");
		break;
default: System.out.println("Hibás értéket adtál meg!!!");
		break;
}
System.out.println();

sc.close();
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
