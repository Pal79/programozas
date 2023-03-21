- [php menü](../php.md)
- [főmenü](../../README.md)

---

```
function arrPrint($arr) {
    for($i = 0; $i < count($arr); $i++) {
        echo $arr[$i] . "<br>";
    }
}

$nums = array(4,15,20,32,55,1,8,7,56,9);

sort($nums);
echo "Számok növekvő sorrendben: <br>";
arrPrint($nums);

echo "<hr>";

rsort($nums);
echo "Számok csökkenő sorrendben: <br>";
arrPrint($nums);

$letters = array("r","é","k","e","l","a","w","z");

sort($letters);
echo "Betűk abc sorrendben: <br>";
arrPrint($letters);

echo "<hr>";

rsort($letters);
echo "Betűk fordított sorrendben: <br>";
arrPrint($letters);


echo "<hr><hr>";

function assocArrPrint($arr) {
    foreach($arr as $key => $value) {
        echo "név: " . $key . ", életkor: " . $value . ";<br>";
    }
}

$names = array(
    "Máté" => 17,
    "Erika" => 42,
    "Dani" => 42,
    "Gyula" => 25,
    "Ági" => 85
);
asort($names);
echo "Nevek és életkorok, életkorok alapján növekvő sorrendben:<br>";
assocArrPrint($names);

echo "<hr>";

arsort($names);
echo "Nevek és életkorok, életkorok alapján csökkenő sorrendben:<br>";
assocArrPrint($names);

echo "<hr>";

ksort($names);
echo "Nevek és életkorok abc sorrenden:<br>";
assocArrPrint($names);

echo "<hr>";

krsort($names);
echo "Nevek és életkorok abc fordított sorrendben:<br>";
assocArrPrint($names);

echo "<hr>";
```

---

- [php menü](../php.md)
- [főmenü](../../README.md)

---
