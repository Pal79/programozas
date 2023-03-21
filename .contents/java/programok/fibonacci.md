- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---

## Fibonacci.java

```
public class Fibonacci {
	
	private int fibonacci(int num) {
		// alaphelyzet
		if (num <= 1) {
			return num;
		}
		// rekurzív behívás
		return fibonacci(num - 1) + fibonacci(num - 2);
	}
	
	public void fibonacciWriteConsole() {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		
		System.out.print("Írj be egy egész számot (meddig íratod ki): ");
		try {
			Integer number = Integer.parseInt(br.readLine());
			
			if(number <= 0) {
				System.out.println("A megadott szám nem lehet nulla vagy mínusz szám.");
			} else {
				for(int i = 0; i < number; i++) {
						System.out.print(fibonacci(i) + " ");
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
		
		Fibonacci fibo = new Fibonacci();
		
		fibo.fibonacciWriteConsole();
	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
