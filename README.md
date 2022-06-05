
// atm programı
import java.util.Scanner;

public class main1 {
	public static void main(String[] args) {
		
		Scanner scanner = new Scanner(System.in);
		
		int bakiye = 1000;
		String islemler = "1. İşlem : Bakiye Öğrenme\n"
				          + "2. İşlem : Para Çekme\n"
				          + "3. İşlem : Para Yatırma\n"
				          + "Çıkış için q'a basın";
		
		System.out.println("***********************************");
		System.out.println(islemler);
		System.out.println("***********************************");
		
		while(true) {
		
			System.out.println("İşlemi seçiniz: ");
			String islem = scanner.nextLine();
		
		if (islem.equals("q")) {
			System.out.println("Programdan Çıkılıyor...");
			break;
		}
		else if (islem.equals("1")) {
		     System.out.println("Bakiyeniz : " + bakiye);
	    }
		else if (islem.equals("2")) {
			 System.out.println("Çekmek İstediğiniz Tutar : ");
			 int tutar = scanner.nextInt();
			 scanner.nextLine(); // başa dönüp nextline alacak bunun önüne geçmek için direk burada yazıyoruz!
			 
			 if (bakiye - tutar < 0) {
				 System.out.println("Yeterli Bakiye Yok! Bakiyeniz : " + bakiye);
			 }
			 else
				 bakiye -= tutar;
			 System.out.println("Yeni bakiyeniz : " +bakiye);
		}
		else if (islem.equals("3")) {
			System.out.println("Yatırmak istediğiniz tutar: ");
			int tutar = scanner.nextInt();
			scanner.nextLine();
			
			bakiye += tutar;
			
			System.out.println("Yeni Bakiyeniz : " +bakiye);
			
		}
		else {
			System.out.println("Geçersiz İşlem...");
		}
	}
	
  }
}






// kullanıcı adı ve parola programı

import java.util.Scanner;

public class main1 {
	public static void main(String[] args) {
		
		Scanner scanner = new Scanner(System.in);
		
		int giris_hakki = 3;
		
		String sys_kullanici_adi = "Mustafa Mert";
		String sys_parola = "12345";
		
		System.out.println("******************************");
		System.out.println("KULLANICI GİRİŞİNE HOŞGELDİNİZ...");
		System.out.println("******************************");
		
		while (true) {
		System.out.println("Kullanıcı Adı : ");
		String kullanici = scanner.nextLine();
		System.out.println("Parola : ");
		String parola = scanner.nextLine();
			
		parola.equals(sys_parola); //eşit mi diye kontrol ediyor
		
		if (kullanici.equals(sys_kullanici_adi) && parola.equals(sys_parola)) {
		System.out.println("Hoşgeldiniz, " + kullanici);
		break;
		}
		
		else if (kullanici.equals(sys_kullanici_adi) && !parola.equals(sys_parola)) { //kullanıcı adı doğru ancak parola ! işareti olunca eşit değilse oluyor;
   System.out.println("Parolanız Yanlış...");
   giris_hakki -= 1;
   
        }
		else if (!kullanici.equals(sys_kullanici_adi) && parola.equals(sys_parola)) {
			
			System.out.println("Kullanıcı Adınız Yanlış...");
			giris_hakki -= 1;
		}
		else {
			System.out.println("Kullanıcı adınız ve parolanız yanlış...");
			giris_hakki -=1;
		}
		
		if (giris_hakki == 0) {
			System.out.println("Giriş hakkınız bitti. Tekrar bekleriz...");
			break;
		}
		}
			
		}
}
