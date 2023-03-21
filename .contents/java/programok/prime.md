- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---

## IsPrime.java

```
public class IsPrime {
	
	boolean prime = true;
	
	public void isPrime(int num) {
		if(num == 0 || num == 1) {
			System.out.println("Az adott szám \"" + num + "\" nem prímszám!");
			prime = false;
		} else {
			for(int i = 2; i <= Math.sqrt(num); i++) {
				if(num % i == 0) {
					prime = false;
					System.out.println("Az adott szám \"" + num + "\" nem prímszám!");
					break;
				}
			}
		}
		
		if(prime == true) {
			System.out.println("Az adott szám \"" + num + "\" prímszám!");
		}
	}
	
	public void primesWriteOutAndCount(int num) {
		int count = 0;
		
		System.out.print("Prímszámok 1 és " + num + " között: ");
		for(int i = 2; i <= num; i++) {
			prime = true;
			
			for(int j = 2; j <= i/2; j++) {
				if(i % j == 0) {
					prime = false;
					break;
				}
			}
			if(prime == true) {
				count++;
				System.out.print(i + " ");
			}
		}
		System.out.println();
		
		System.out.println("Összesen " + count + " darab prímszám van 1 és " + num + " között!");
	}
}
```

---

## Main.java

```
public class Main {

	public static void main(String[] args) {
		
		IsPrime prime = new IsPrime();
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		
		try {
			System.out.print("Kérlek adj meg egy egész számot, hogy megtudd, prímszám e az adott szám: ");
			int num = Integer.parseInt(br.readLine());
			prime.isPrime(num);
			
			System.out.print("Kérlek adj meg egy számot, hogy megtudd, mely prímszámok vannak 1 és a megadott szám között: ");
			num = Integer.parseInt(br.readLine());
			prime.primesWriteOutAndCount(num);
		} catch (NumberFormatException e) {
			System.out.println("Egész számot kell megadni!");
		} catch (IOException e) {
			System.out.println("IO kivételes hiba történt!");
		}

	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
