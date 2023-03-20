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
