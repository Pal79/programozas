- [java menü](../../java.md)
- [Főmenü](../../../README.md)

# Kivételkezelés

```
private static BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

public static void main(String[] args) {

	/**************************************************************
	 * KIVÉTELKEZELÉS
	 * 
	 * Átvesszük a hiba kezelését a fordítótól,
	 * hogy egy általunk meghatározott módon oldjunk meg egy hibát
	 * 
	**************************************************************/

	int szamBekert = 0;

	try {
		System.out.println("Kérem adjon meg egy egész számot: ");

		/*********************************************************************
		 * Ebbe a blokkba helyezzük azokat a kódokat, amelyek hibát dobhatnak.
		 * Az itt deklarált változó lokális lesz, a blokkon kivül nem elérhető
		 * 
		 * br.close(); //null lesz a br értéke
		 * ez a sor definíció: a szamBekert változó értéket kapja
		 * 
		 ********************************************************************/

		szamBekert = Integer.parseInt(br.readLine());
		System.out.println("A megadott szám ez volt: " + szamBekert);			
	} catch (NumberFormatException e) {
		/*****************************************
		 * ha nem egész számot adok meg, 
		 * hanem pld. törtszámot vagy karaktereket
		 ****************************************/
		//e.printStackTrace();
		System.out.println("Egész számot kértem!!!");
	} catch (IOException e) {
		/***********************************************
		 * Ha korábban zárjuk be az olvasó adatfolyamot. 
		 **********************************************/
		// e.printStackTrace();
		System.out.println("IO hiba");
	} catch (Exception e) {
		/*********************
		 *  Bármilyen más hiba
		 ********************/
		System.out.println("Bármilyen hiba");
	} finally {
		/*************************************************
		 * nem kötelező része a try-catch blokknak
		 * mindenképpen lefut
		 * tisztogatásra, memória terület felszabadítására
		 ************************************************/
		System.out.println("Kivételkezeléssel megoldott adatbekérés!");
	}
	System.out.println(szamBekert);
	/*
	 * Speciálistól megyünk az általánosabbig
	 */

	/**************************************************************************************
	 * További kivételkezelő osztályok:
	 * 
	 * ArrayIndexOutOfBoundsException: - olyan elemre hivatkozok a tömbön belül, ami nincs
	 * IOException: IO hiba, fájlkezelés és olvasó/író adatfolyamok
	 * FileNotFoundException: - nem találja a fájlt a megadott elérési úton és névvel
	 * ArithmeticException - Nullával való osztás és matematikai kivételek
	 *************************************************************************************/

	/***********************************************************************************
	 * Feladat: 
	 * kérjünk be két egész számot hibakezeléssel, majd osszuk el az elsőt a másodikkal!
	 * 0-val való osztásra figyeljünk!
	 **********************************************************************************/
	System.out.println();
	System.out.println("2. feladat:");
	try {
		System.out.println("Kérem adja meg az osztandót(egész szám): ");
		int osztando = Integer.parseInt(br.readLine());

		System.out.println("Kérem adja meg az osztót(egész szám): ");
		int oszto = Integer.parseInt(br.readLine());

		double eredmeny = (double)osztando/oszto;

		System.out.println(eredmeny);
	} catch (NumberFormatException e) {
		// TODO Auto-generated catch block
		//e.printStackTrace();
		System.out.println("Nem egész számot adtál meg!!!");
	} catch (ArithmeticException e) {
		// TODO Auto-generated catch block
		//e.printStackTrace();
		System.out.println("0-val való osztás tiltott!!!");
	} catch (IOException e) {
		// TODO Auto-generated catch block
		e.printStackTrace();
	} catch (Exception e) {
		// TODO Auto-generated catch block
		//e.printStackTrace();
		System.out.println("Valamilyen hiba történt...");
	}

	try {
		br.close();
	} catch (IOException e) {
		// TODO Auto-generated catch block
		e.printStackTrace();
	}

	/*****************************************************************S
	 * A kivételeknek két csoportja: 
	 * 
	 * - checked: pld. IO műveletek - fordítási időben dobnak hibát
	 * - unchecked: futási idöben dob hibát pl.: NumberFormatException
	 ****************************************************************/
}
```

---

- [java menü](../../java.md)
- [Főmenü](../../../README.md)

---
