---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)


# Véletlen számok

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

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
