- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---

## Prime.java

```
public class Prime {
	
boolean prime = true;
	
	public String isPrime(int num) {
		String result = "";
		
		if(num == 1 || num == 2) {
			result = "A megadott szám: " + num + " nem prímszám."; 
			prime = false;
		} else {
			for(int i = 2; i <= Math.sqrt(num); i++) {
				if(num % i == 0) {
					prime = false;
					result = "A megadott szám: " + num + " nem prímszám.";
					break;
				}
			}
		}
		
		if(prime == true) {
			result = "A megadott szám: " + num + " prímszám.";
		}
		
		return result;
	}

}
```

---

## SieveOfEratosthenes.java

```
public class SieveOfEratosthenes {
	
	public void sieveOfEratosthenes() {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		
		System.out.print("Megddig írjuk ki a prímeket: ");
		try {
			Integer maxNumber = Integer.parseInt(br.readLine());
			
			Boolean[] arr = new Boolean[maxNumber +1];
			arr[0] = false;
			arr[1] = false; // 0 és 1 false alapból 
			
			for(int i = 2; i <= maxNumber; i++) {
				arr[i] = true; // mindent igazra állítok
			}
			
			for(int i = 2; i * i <= maxNumber; i++) {
				if(arr[i]) {
					// prím többszörösei kiszitálása
					for (int j = i * i; j <= maxNumber; j += i) {
						arr[j] = false;
					}
				}
			}
			
			for(int i = 0; i <= maxNumber; i++) {
				if(arr[i]) { // amennyiben igaz, kiírjuk a számot
					System.out.print(i + " ");
				}
			}
			
			br.close();
			
		} catch (NumberFormatException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}

}
```

---

## Main.java

```
public class Main {
	
	private static BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

	public static void main(String[] args) {
		
		Prime primeObj = new Prime();
		SieveOfEratosthenes erathosObj = new SieveOfEratosthenes();
		
		try {
			System.out.print("Adj meg egy számot: ");
			int num = Integer.parseInt(br.readLine());
			
			System.out.println(primeObj.isPrime(num));
			
			erathosObj.sieveOfEratosthenes();
		} catch (NumberFormatException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
