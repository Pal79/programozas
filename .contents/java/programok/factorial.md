- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---

## Factorial.java

```
public class Factorial {
	
	public Integer factorial(int num) {
		if(num == 1) {
			return 1;
		}
		return num * factorial(num - 1);
	}
	
	public BigInteger factorialWithBigInt (int num ){
	    if (num < 0) {
	        return BigInteger.ZERO;
	    } else if (num==0){
	        return BigInteger.ONE;
	    } else {
	        return BigInteger.valueOf(num).multiply(factorialWithBigInt(num-1));
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

		Factorial factorialObj = new Factorial();
		
		System.out.print("Adj meg egy számot: ");
		
		try {
			Integer number = Integer.parseInt(br.readLine());
			
			// 34 -től 0 az eredmény
			if(number >= 34) {
				System.out.println(number + "! = " + factorialObj.factorialWithBigInt(number));
			} else {
				System.out.println(number + "! = " + factorialObj.factorial(number));
			}
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
