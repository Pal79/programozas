---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---



### Alapvető típusok

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

### Boolean - Logikai típus

> csak igaz/hamis értéket vehet fel (true vagy false) 1 vagy 0

```
boolean registered = false;
System.out.println(registered); // kimenet: false

boolean sold;
sold = true;

System.out.println(sold); // kimenet: true
```

### Szöveg és karakterek - String és char


```
char letter = 'R'; //szimpla aposztrof
//char letterError = "K"; //hiba

System.out.println(letter); // kimenet: R
```

### Kiírás és hozzáfűzés + operátorral

```
String text;
text = "teszt szöveg";
System.out.println("A text változó tartalma: " + text + "...");
```

### String literál felvétele

```
String text2 ="Teszt szöveg2";
System.out.println(text2);
```

```
String text3 = "Ez egy java \n String (új sorban...)";
System.out.println(text3);
```

### speciális karakterek

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

### Egész számok - primitív típus

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

### int vs Integer

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

### Double

> 3.0 ADATVESZTÉS (egész számot egész számmal osztottam):

```
double fraction = 10/3;
System.out.println(fraction);
```

##### Hogyan lehet megoldani?

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

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
