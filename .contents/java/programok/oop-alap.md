- [java menü](../../java.md)
- [Főmenü](../../../README.md)

> Henger.java

```
public class Henger {
```

- I. rész: adattagok, mezők (fields)

```
	private int magassag;
	private int sugar;
```

- II. rész konstruktor(ok) deklaráció
- Konstruktor: az osztállyal azonos nevű, publikus metódus 
- Inicializálja (beállítja) az objektumpéldány alapértékeit
- Akkor kerül meghívásra, amikor létrejön az objektumpéldány (new)
- Fontos szabály: komoly üzleti logikát nem szabad beletenni (ciklus, elág)
- Mert probléma lehet, ha nem jön létre az objektumpéldány 
- Paraméterrel vagy paraméter nélkül is deklarálhatjuk.

```
	public Henger(int magassag, int sugar) {
		//this - az objektumpéldányra utal
		this.magassag = magassag;
		this.sugar = sugar;
	}
```

- III. rész: getters/setters: tulajdonságok (property)
   - get -> lekérdezések
   - set -> beállítások

```
	public int getMagassag() {
		return magassag;
	}

	public void setMagassag(int magassag) {
		this.magassag = magassag;
	}

	public int getSugar() {
		return sugar;
	}

	public void setSugar(int sugar) {
		this.sugar = sugar;
	}
```

- IV. rész: saját metódusok

```
	public double getFelszin() {
		return 2*(Math.pow(this.sugar, 2)*Math.PI)+this.magassag*2*this.sugar*Math.PI;
	}
	
	public double getTerfogat() {
		return Math.pow(this.sugar, 2)*Math.PI*this.magassag;
	}
	
	public void terfogatKiir() {
		System.out.println("A henger térfogata: " + getTerfogat());
	}
}
```

> TomorHenger.java

```
public class TomorHenger extends Henger {
```

- származtatás: extends kulcsszóval történik
- A TomorHenger (gyermek osztály) megörökli az ősosztálytól (Henger)
- annak tulajdonságait és viselkedésformáit

```
	private double suruseg;

	public TomorHenger(int magassag, int sugar, double suruseg) {
		super(magassag, sugar);
		this.suruseg = suruseg;
	}

	public double getSuruseg() {
		return suruseg;
	}

	public void setSuruseg(double suruseg) {
		this.suruseg = suruseg;
	}
```

- kiegészítjuk az ősosztály viselkedését

```
	public double getTomeg() {
		return this.suruseg*this.getTerfogat();
	}
```

- felülírás: az ősosztályban lévő ugyanilyen nevű metódust írjuk felül

```
	public void terfogatKiir() {
		System.out.println("A tömörhenger térfogata: " + this.getTerfogat());
	}
}
```

> Cso.java

```
public class Cso extends TomorHenger {

	private int belsoSugar;

	public Cso(int magassag, int sugar, double suruseg, int belsoSugar) {
		super(magassag, sugar, suruseg);
		this.belsoSugar = belsoSugar;
	}

	public int getBelsoSugar() {
		return belsoSugar;
	}

	public void setBelsoSugar(int belsoSugar) {
		this.belsoSugar = belsoSugar;
	}

	public double getTerfogat() {
		return new Henger(this.getMagassag(), this.getSugar()).getTerfogat() - new Henger(this.getMagassag(), this.getBelsoSugar()).getTerfogat();
	}

	public double getFelszin() {
		return super.getFelszin()+(new Henger(this.getMagassag(), this.belsoSugar)).getFelszin() - 4*Math.pow(this.belsoSugar, 2)*Math.PI;
	}

}
```

> Main.java

```
public class Main {
```

> Program belépési pontja - main

```
	public static void main(String[] args) {
```

- hengerObj néven létrejön az objektumpéldány
- magasság 10-es érték, sugár 1-es értékkel
- konstruktor hívás

```
		Henger hengerObj = new Henger(10, 1);
		//hengerObj.setMagassag(20);
		hengerObj.terfogatKiir();

		System.out.println("Henger felszín: " + hengerObj.getFelszin());
		System.out.println("Henger térfogat: " + hengerObj.getTerfogat());
		System.out.println("Henger magassága: " + hengerObj.getMagassag());


		TomorHenger tomorHengerObj = new TomorHenger(10, 2, 0.5);

		System.out.println("Tömörhenger felszín: " + tomorHengerObj.getFelszin());
		System.out.println("Tömörhenger térfogata: " + tomorHengerObj.getTerfogat());
		System.out.println("Tömörhenger tömeg: " + tomorHengerObj.getTomeg());

		tomorHengerObj.terfogatKiir();


		Cso csoObj = new Cso(10, 2, 0.5, 1);

		System.out.println("Cső térfogata: " + csoObj.getTerfogat());
		System.out.println("Cső felszín: " + csoObj.getFelszin());
		
	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
