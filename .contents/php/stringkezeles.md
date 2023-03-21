- [php menü](../php.md)
- [főmenü](../../README.md)

---

## Stringkezelés


> Egyszerű kiíratás

```
$hello = "Hello World!!!";
```

---

> string karakterek száma

```
echo "strlen - " . $hello . ": " . strlen($hello) . " - string karakterek száma<hr>";
```

---

> hány szóból áll

```
echo "str_word_count - " . $hello . ": " . str_word_count($hello) . " - hány szóból áll<hr>";
```

---

> visszafele írja ki (pl.: palindromoknál)

```
echo "strrev - " . $hello . ": " . strrev($hello) . " - visszafele írja ki<hr>";
```

---

> hányadik indexnél kezdődik az adott elem

```
echo "strpos(String, keresett) - " . $hello . ": " . strpos($hello, "World") . " - hányadik indexnél kezdődik az adott elem<hr>";
```

---

> lecseréli az adott elemet a megadottra

```
echo "str_replace(mit, mire, miben) - " . $hello . " -> Ave World!!!: " . str_replace("Hello", "Ave", $hello) . " - lecseréli az adott elemet a megadottra<hr>";
```

---

> összekeveri a megadott elemeket (pl. jelszavak generálásánál)

```
echo "str_shuffle - " . $hello . ": " . str_shuffle($hello) . " - összekeveri a megadott elemeket<hr>";
```

---

> adott számú elemet ad vissza

```
echo "substr(miben, mettől, meddig) - " . $hello . ": " . substr($hello, 1, 4) . " - adott számú elemet ad vissza<hr>";
```

---

> az adott adatok hány százalékban egyeznek

```
$var1 = "szipi szupi jó minden";
$var2 = "elég szuper minden";
similar_text($var1, $var2, $result);
echo "similar_text(param1, param2, eredmény): " . $result . " - az adott adatok hány százalékban egyeznek<hr>";
```

---

> kisbetűs kiírás

```
echo "strtolower - " . $hello . ": " . strtolower($hello) . " - csak kisbetűs kiírás<hr>";
```

---

> nagybetűs kiírás

```
echo "strtoupper - " . $hello . ": " . strtoupper($hello) . " - csak nagybetűs kiírás<hr>";
```

---

- [php menü](../php.md)
- [főmenü](../../README.md)

---
