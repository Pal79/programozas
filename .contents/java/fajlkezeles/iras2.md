- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Írás 2

```
public static void main(String[] args) {
		
		try {
			FileOutputStream fs = new FileOutputStream("gumiKacsa/tomb.txt");
			OutputStreamWriter out = new OutputStreamWriter(fs, "UTF-8");
			
			int[] tomb = {33,15,19,21};
			
			for (int item : tomb) {
				out.write(String.valueOf(item));
				out.write(" ");
			}
			
			out.close();
			fs.close();
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			//e.printStackTrace();
		} catch (UnsupportedEncodingException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		System.out.println("Létrejött a tomb.txt nevű fájl a gumiKacsa mappán belül!");
		
	}

}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
