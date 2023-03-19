<details>
<summary>Alapok</summary>

---

<details>
<summary>Típusok</summary>

---

# Alapvető típusok

| Primitív típus | Osztály | Leírás | min | max |
| :------------- | :------ | :----- | :-- | :-- |
| boolean | Boolean | logikai típus | true | false |
| char | Character | 16 bites UNICODE | karakter | karakter |
| byte | Integer | 8 bites előjeles egész | -128 | +127 |
| short | Integer | 16 bites előjeles egész | -32_768 | +32_767 |
| int | Integer | 32 bites előjeles egész | | -2_147_483_648 | +2_147_483_647 |
| long | Integer | 64 bites előjeles egész | -9_223_372_036_854_775_808 | +9_223_372_036_854_775_807 |
| float | Float | 32 bites lebegőpontos szám | -3,40292347E+38 | +3,40292347E+38 |
| double | Double | 64 bites lebegőpontos szám | -1,79769313486231570E+308 | +1,79769313486231570E+308 |

> osztályonként konstansok definálják a határokat

> egész számok: MIN_VALUE és a MAX_VALUE

> float és double: POSITIVE_INFINITY és a NEGATIVE_INFINITY

# Boolean - Logikai típus

> csak igaz/hamis értéket vehet fel (true vagy false) 1 vagy 0

```
boolean registered = false;
System.out.println(registered); // kimenet: false

boolean sold;
sold = true;

System.out.println(sold); // kimenet: true
```

# Szöveg és karakterek - String és char


```
char letter = 'R'; //szimpla aposztrof
//char letterError = "K"; //hiba

System.out.println(letter); // kimenet: R
```

# Kiírás és hozzáfűzés + operátorral

```
String text;
text = "teszt szöveg";
System.out.println("A text változó tartalma: " + text + "...");
```

# string literál felvétele

```
String text2 ="Teszt szöveg2";
System.out.println(text2);
```

```
String text3 = "Ez egy java \n String (új sorban...)";
System.out.println(text3);
```

# speciális karakterek

- \\n - sortörés
- \\t - tabulátor
- \\b - backspace

```
System.out.println(text + "\"\t" + text2);
```

```
System.out.println(text.contains("Teszt")); //false
```

### Stringek összehasonlítása

> == javaban nem működik (hashkódokat hasonlít össze)
> equals - metódussal kell megoldani

```
System.out.println(text.equals("teszt szöveg")); //true
System.out.println(text.equals(szoveg2)); //false
```

> if (szoveg==szoveg2) - EZ NEM JÓ

> if (szoveg.equals(szoveg2)) - Így kell megoldani

> String immutable object - nem lehet megváltoztatni a karaktereket
> elérni el tudom (lekérdezni le tudom), de megváltoztatni nem

```
String name = "Teszt Elek";
System.out.println(name.charAt(0)); //name.charAt(0) = 't';
```

> felílárást - StringBuilder osztállyal lehet megoldani

# Egész számok - primitív típus

> deklaráció: number nevű változó, amelynek típusa egész szám

```
int number;
```

> definíció: a number változó értéket kap

```
number = 100;
```

> deklaráció és definíció

```
int number2 = 200;
```

> \+ operátor: összefűzés (konkannetáció)

```
System.out.println("Két szám összege: " + number + number2);
```

> kimenet: 100200

```
System.out.println("Két szám összege: " + (number + number2));
```

> kimenet: 300

# int vs Integer

> int -> primitív tipus
> Integer -> object


> érték tipus (mem. tárolás)

```
@SuppressWarnings("unused")
int primitiveNumber = 44;
```

> referencia tipus (mem. tárolás)
```
@SuppressWarnings("unused")
Integer numberObject = 55;
```

> int szamPrimitívTeszt = null; //hibára fut

```
@SuppressWarnings("unused")
Integer szamObjTeszt = null;
int szamPrimitivTeszt2 = 0;
```

# Double

> 3.0 ADATVESZTÉS (egész számot egész számmal osztottam):

```
double fraction = 10/3;
System.out.println(fraction);
```

### Hogyan lehet megoldani?
		
> 1. Megoldás

```
double fraction1 = 10.0/3;
System.out.println(fraction1);
```

> 2. Megoldás

```
double fraction2 = 10/3f;
System.out.println(fraction2);
```

> 3. Megoldás

```
double fraction3 = 10/3d;
System.out.println(fraction3);
```

> 4. Megoldás: típuskényszerítés: kasztolás 

```
double fraction4 = (double)10/3;
System.out.println(fraction4);
```

</details>

<details>
<summary>OPERÁTOROK -> műveletvégző "jelek"</summary>

---

> OPERANDUS -> amiken a műveleteket végezzük

```
int result = a + b; //a és b operandus, + =
```

> értékadó operátor, egy darab =


int number1 = 5;
int number2 = 10;


> Matematikai operátorok

> + -  * / (egész osztás) % (MOD) modulo - maradékképzés

```
System.out.println("Összege: " + (number1 + number2));
int difference = number2 - number1;
System.out.println("Különbség: " + difference);
```
		
> maradékképzés - MOD: modulo

```
System.out.println(5 % 7); //5
System.out.println(4 % 2); //0
System.out.println(6 % 2); //0
System.out.println(2 % 1); //0
System.out.println(12 % 5); //2
```

> Értéknövelő (inkrementálás) és értékcsökkentő(dekrementálás)

> * ++ és --
> prefix és postfix

```
int szam3 = 7;
System.out.println(++szam3); //8
System.out.println(szam3++); //8
System.out.println(szam3); //9
```

> balérték - jobbérték (right value, left value)
   > mindig a baloldalon álló kifejezés veszi a jobboldalon állót

```
int a = 10;
int b = 12;
a = b;
System.out.println(a); //12
```
		
		
> Relációs operátorok (összehasonlító operátorok) - elágazásoknál
> < > <= >= !=(nem egyenlő)  == (egyenlőség)
		
> Logikai operátorok - Bool algebra műveletei

- ÉS (AND) -> && - altgr+c
- VAGY (OR) -> || - altgr +w
- Negálás (Tagadás) -> !
- Kizáró vagy -> XOR

```
boolean A = true;
boolean B = false;

System.out.println("A és B értéke: " + (A && B)); //false
System.out.println("A vagy B értéke: " + (A || B)); //true
System.out.println("A értékének tagadása: " + !A); //false

System.out.println(A && B || A); //true
System.out.println(A || (B && A)); //true

System.out.println(5 == 7); //false
System.out.println(5 <= 5); //true
```
		
> Operátorok sorrendisége (precedenciája)

- általában a matematika szabályai érvényesek
- érdemes zárójelezni
- értékadásnál jobbról balra történik a végrehajtás
- alapértelmezetten pedig balról jobbra

- i++, i-- postix értéknövelés, értékcsökkentés
- ++i, --i prefix értéknövelés, értékcsökkentés
- * /
- + -
- biteltolás
- összehasonlító operátorok -> <> <= stb.
- egyenlőség vizsgálat -> == !=
- Bitműveletek -> AND OR XOR
- Logikai műveletek és -> && AND
- Logikai műveletek vagy -> || OR
- ternary operator -> (short if) kifejezés(logikai) ? igaz: hamis
- értékadás

</details>

<details>
<summary>Számítások</summary>

---

# Math osztály elemei

### hatványozás

```
System.out.println(Math.pow(2, 3)); //8.0
```

### gyökvonás

```
System.out.println(Math.sqrt(25)); //5.0
```

### Pi értéke (nem 3.14)

```
System.out.println(Math.PI);
```

### abszolútérték

```
int abszulutErtek = Math.abs(-44);
System.out.println(abszulutErtek); //44
```

> **hiba** -> int eredmeny = Math.pow(2, 3);

```
double eredmeny = Math.pow(2, 3);
```

### Kerekítések

> Round - matematika szabályai szerint kerekít
System.out.println(Math.round(24.5)); //25

> lefelé kerekítés

```
System.out.println(Math.floor(24.9)); //24.0
```

> felfelé kerekítés

```
System.out.println(Math.ceil(24.1)); //25.0
```

</details>

<details>
<summary>Véletlen számok generálása</summary>

---

> new operátor memória terület foglalás - példányosítás

> r néven létrejön az objektum

> pszeudó véletlen szám - ál véletlen

```
Random r = new Random();
```

> egy db véletlen szám generálása 1-100 között

```
int tesztVelSzam = r.nextInt(100)+1;
System.out.println("Véletlen szám 1-100: " + tesztVelSzam);
```

> 1-2 közötti tartományban véletlen szám:

```
int tesztVelSzam2 = r.nextInt(2)+1;
System.out.println("Véletlen szám 1-2: " + tesztVelSzam2);
```

> 5-10 közötti tartományban véletlen szám:

```
int tesztVelSzam3 = r.nextInt((10-5)+1)+5;
System.out.println("Véletlen szám 5-10: " + tesztVelSzam3);
```

> Általános képlet: r.nextInt((max-min)+1)+min;

</details>

<details>
<summary>Kiírás, beolvasás</summary>

---

# Scanner és BufferedReader

- Scanner a régebbi osztály, BufferedReader az újabb
- BufferedReader - gyorsabb a feldolgozás, szálbiztos, szinkronizált és többszálú

### SCANNER

- System.in - standard bemenet - billentyűzet
- scObj néven létrejön egy objektumpéldány,
- new kulcsszó memória terület foglalást jelent

```
Scanner scObj = new Scanner(System.in);
		
/* szöveg beolvasása Scanner osztállyal */
System.out.println("Kérem adja meg a nevét(Scanner): ");
String beolvasottNev = scObj.nextLine();

System.out.println("A megadott név ez volt: " + beolvasottNev);
```
		
- egész szám beolvasása Scanner osztállyal:
- konvertálásra is szükség van ami a billentyűzetről érkezik az String,
- ha ettől eltérő típusba szeretném tárolni
- akkor konvertálnom kell

```
System.out.print("Adja meg az életkorát(egész szám)(Scanner): ");
int eletKor = Integer.parseInt(scObj.nextLine());

System.out.println("Kor: " + eletKor);
```

> törtszám beolvasása Scanner és átalakítással

```
System.out.print("Kérem adja meg a súlyát(törtszám)(Scanner): ");
double testSuly = Double.parseDouble(scObj.nextLine());
		
System.out.println("Testsúly: " + testSuly);
```

### BUFFEREDREADER

```
BufferedReader brObj = new BufferedReader(new InputStreamReader(System.in));
```

> szöveg beolvasása BufferedReader osztállyal

```
System.out.print("Adja meg a nevét (BufferedReader): ");
String beolvasottNev2 = brObj.readLine();

System.out.println("A megadott név(Br): " + beolvasottNev2);
```

> egész szám beolvasása BufferedReader osztállyal és konvertálással

```
System.out.print("Kérem adja meg a magasságát(cm) - egész szám (BufferedReader): ");
int magassag = Integer.parseInt(brObj.readLine());

System.out.println("A megadott magasság(BR): " + magassag + "cm");
```

> törtszám beolvasása BufferedReader osztállyal és konvertálással

```
System.out.print("Adja meg a cipőméretét (törtszám): ");
double cipoMeret = Double.parseDouble(brObj.readLine());

System.out.println("A cipő mérete: " + cipoMeret);
```

> bezárja a brObj-et

```
brObj.close();
```

> bezárja a scObj-ektet- memória terület felszabadítás

```
scObj.close();
```

</details>

<details>
<summary>Elágazások</summary>

---

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

</details>

<details>
<summary>Ciklusok</summary>

---

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

</details>

---

</details>


<details>
<summary>Programozási tételek</summary>

---

<details>
<summary>Eldöntés</summary>

---

- egy halmazon belül vizsgáljuk,
- hogy egy érték benne van,
- vagy nincs.

- true/false

```
public static boolean decide(int[] arr, int search) {
	boolean answer = false;
	int i = 0;

	while (i < arr.length && arr[i] != search) {
		i++;
	}

	if (i < arr.length) {
		answer = true;
	}
	return answer;
}

public static void main(String[] args) {
	int search = 10;
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	if(decide(arr, search)) {
		System.out.println("Az adott szám: " + search + " benne van a tömbben.");
	} else {
		System.out.println("Az adott szám: " + search + " nincs benne a tömbben.");
	}
}
```
 
</details>

<details>
<summary>Kiválasztás</summary>

- egy sorozatban keresünk egy elemet,
- de biztosan tudjuk, hogy valahol benne van.

```
public static int selection(int[] arr, int search) {
	int i = 0;
	while (arr[i] != search) {
		i++;
	}
	return i;
}

public static void main(String[] args) {
	int index = 10;
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	System.out.println("A keresett szám indexe: " + selection(arr, index));
}
```

</details>

<details>
<summary>Kiválogatás</summary>

---

- egy halmaz elemei közül kiválogatjuk
- az adott tulajdonságú elemket

```
public static int evenPieceCount(int[] arr) {
	int count = 0;
	for (int item : tomb) {
		if (item %2==0) {
			count++;
		}
	}
	return count;
}

public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	System.out.print("A tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	int[] evenArray = new int[evenPieceCount(arr)];
	int[] unmatchedArray = new int[arr.length - evenPieceCount(evenArray)];
	int evenIndex = 0;
	int unmatchedIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] % 2 == 0) {
			evenArray[evenIndex] = arr[i];
			evenIndex++;
		} else {
			unmatchedArray[unmatchedIndex] = arr[i];
			unmatchedIndex++;
		}
	}

	System.out.print("A tömb páros elemei: ");
	for(int item : evenArray) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("A tömb páratlan elemei: ");
	for(int item : unmatchedArray) {
		System.out.print(item + " ");
	}
}
```

</details>

<details>
<summary>Maximum kiválasztás</summary>

---

- egy halmazon belül keressük
- a legnagyobb értékű elemet.

- kiegészítés: Melyik indexen van a legnagyobb érték?

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	int max = arr[0];
	int maxIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] > max) {
			max = arr[i];
			maxIndex = i;
		}
	}
	System.out.println("Maximum érték a tömbben: " + max + "\nMaximum érték indexe: " + maxIndex);
}
```

</details>

<details>
<summary>Minimum kiválasztás</summary>

---

- Egy halmazon belül keressük a legkisebb értékű elemet

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};

	int min = arr[0];
	int minIndex = 0;

	for(int i = 0; i < arr.length; i++) {
		if(arr[i] < min) {
			min = arr[i];
			minIndex = i;
		}
	}
	System.out.println("Minimum érték a tömbben: " + min + "\nMinimum érték indexe: " + minIndex);
}
```

</details>

<details>
<summary>Megszámlálás</summary>

---

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

</details>

<details>
<summary>Metszet</summary>

---

- azoknak az elemeknek a kiválasztása,
- amelyek mind a két halmazban megtalálhatóak.

- Az egyes tömbökön belül nem lehetnek ismétlődések.

```
public static boolean decide(int[] arr, int search) {
	boolean itsIn = false;
	int i = 0;

	do {
		if(arr[i] == search) {
			itsIn = true;
		}
		i++;
	} while(!itsIn && i < arr.length);

	return itsIn;
}

public static int newArraySize(int[] arrA, int[] arrB) {
	// kiderítjük, hány darab egyezés van - ez lesz az új tömb mérete
	int count = 0;

	for(int i = 0; i < arrB.length; i++) {
		if(decide(arrA, arrB[i])) {
			count++;
		}
	}

	return count;
}

public static int[] resultArrListening(int[] arrA, int[] arrB) {
	int[] resultArr = new int[newArraySize(arrA, arrB)];
	int index = 0;

	for(int i = 0; i < arrB.length; i++) {
		if(decide(arrA, arrB[i])) {
			resultArr[index] = arrB[i];
			index++;
		}
	}
	return resultArr;
}

public static void main(String[] args) {
	int[] arrA = {1,2,3,4,5,6,7,8,9,10};
	int[] arrB = {6,7,8,9,10,11,12,13,14,15};

	System.out.print("\"A\" tömb elemei: ");
	for(int item : arrA) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("\"B\" tömb elemei: ");
	for(int item : arrB) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Metszet: ");
	for(int item : resultArrListening(arrA, arrB)) {
		System.out.print(item + " ");
	}
}
```

</details>

<details>
<summary>Összegzés</summary>

---

- Meghatározza egy számsorozat(tömb) elemeinek összegét

```
public static void main(String[] args) {
	int[] arr = {1,2,3,4,5,6,7,8,9,10,11,...};
	int result = 0;

	for(int item : arr) {
		result += item;
	}
	System.out.println(result);
}
```

</details>

<details>
<summary>Unio</summary>

---

- két halmaz elemei közül legalább az egyikben szerepelnie kell.
- A halmazokon belül nincs ismétlődés

```
private static boolean decide(int[] arr, int search) {
	boolean itsIn = false;
	int i = 0;

	do {
		if (arr[i] == search) {
			itsIn = true;
		}
		i++;
	} while (!itsIn && i < arr.length);
	return itsIn;
}

private static int matchesNumbersDefines(int[] arrA, int[] arrB) {
	int count = 0;

	for (int i = 0; i < arrB.length; i++) {
		if (decide(arrA, arrB[i])) {
			count++;
		}
	}
	return count;
}

private static int[] resultArray(int[] arrA, int[] arrB) {
	int arraySize = (arrA.length + arrB.length) - matchesNumbersDefines(arrA, arrB);
	int[] resultArray = new int[arraySize];

	//1.lépés arrA-ból minden elemet belepakolok az eredmenytömbbe
	for(int i = 0; i < arrA.length; i++) {
		resultArray[i] = arrA[i];
	}

	//2. lépés: arrB-ből azokat helyezzük bele, ami még nincs benne
	int resultArraySize = arrA.length;

	for(int i = 0; i < arrB.length; i++) {
		if(!decide(resultArray, arrB[i])) {
			resultArray[resultArraySize] = arrB[i];
			resultArraySize++;
		}
	}
	return resultArray;		
}

public static void main(String[] args) {
	int[] arrA = {1,2,3,4,5,6,7,8,9,10};
	int[] arrB = {6,7,8,9,10,11,12,13,14,15};

	System.out.print("\"A\" tömb elemei: ");
	for(int item : arrA) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("\"B\" tömb elemei: ");
	for(int item : arrB) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Unio: ");
	for(int item : resultArray(arrA, arrB)) {
		System.out.print(item + " ");
	}
}
```

</details>

<details>
<summary>Rendezések</summary>

---

<details>
<summary>Buborékrendezés</summary>

---

```
public static void main(String[] args) {

	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Rendezett tömb elemei: ");
	for(int item : bubbleSort(arr)) {
		System.out.print(item + " ");
	}
}

public static int[] bubbleSort(int[] arr) {
	int temp;

	for(int i = 0; i < arr.length; i++) {
		for(int j = 0; j < arr.length-i-1; j++) {
			if(arr[j] > arr[j+1]) {
				temp = arr[j];
				arr[j] = arr[j+1];	
				arr[j+1] = temp;
			}
		}
	}
	return arr;
}
```

</details>

<details>
<summary>Egyszerű cserés rendezés</summary>

---

```
public static void main(String[] args) {

	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("Tömb elemei rendezve: ");
	for(int item : exchangeSort(arr)) {
		System.out.print(item + " ");
	}
}

private static int[] exchangeSort(int[] arr) {
	for(int i = 0; i < arr.length-1; i++) {
		for(int j = i+1; j < arr.length; j++) {
			if(arr[i] > arr[j]) {
				int temp = arr[j];
				arr[j] = arr[i];
				arr[i] = temp;
			}
		}
	}

	return arr;
}
```

</details>

<details>
<summary>Minimum kiválasztásos rendezés</summary>

---

```
public static void main(String[] args) {
		
	int[] arr = {1,2,3,4,5,6,7,8,9,10,...};

	System.out.print("Tömb elemei: ");
	for(int item : arr) {
		System.out.print(item + " ");
	}
	System.out.println();

	System.out.print("A tömb rendezve: ");
	minChangeSort(arr);
}

private static void minChangeSort(int[] arr) {
	int change;
	int minIndex;

	for (int i = 0; i < arr.length; i++) {
		minIndex = i;
		for (int j = i+1; j < arr.length; j++) {
			if (arr[j] < arr[minIndex]) {
				minIndex = j;
			}
		}
	
		//csere
		if (i != minIndex) {
			change = arr[i];
			arr[i] = arr[minIndex];
			arr[minIndex] = change;
		}
		System.out.print((i+1) + ".futás: ");
		for(int item : arr) {
			System.out.print(item + " ");
		}
		System.out.println();
	}
}
```

</details>

</details>

[Főmenü](../README.md)
