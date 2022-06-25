# Week2Assignment

## ARAŞTIRMA KONUSU (20 puan)
Aşağıdaki bağlantıda yer alan isimlendirme geleneklerinin (naming conventions) arasındaki farkları belirten bir paragraflık yazı yazınız. İfadeleri kendi araştırmalarınız sonucunda yazmanız beklenmektedir.

CEVAP= Yazılım da isimlendirme kuralları çok önemlidir. Çünkü ilerleyen süreçlerde hem kendimiz için hem de bir ekip ile çalışıyorsak ekip arkadaşlarımıza kolaylık sağlar. Kodlarımızı daha sonrasında tekrardan döndüğümüz de zorluk çekmeden okuyup, eklemeler ve değişiklikler yapabiliriz.

camelCase için --> ilk kelimenin ilk harfi küçük harfle başlar sonraki her yeni kelime için ilk harfi büyük olur.
Örnek: camelCase, pascalCase gibi...

PascalCase için --> Camel Case ile aynı sayılabilir aralarında ki tek fark Camel Case'de ilk kelimenin ilk harfi küçükdü, Pascal Case' de her kelimenin ilk harfi büyük olur.
Örnek: PascalCase, CamelCase gibi

## LINUX COMMANDS (4 x 5 = 20 puan)
Aşağıdaki linux komutlarını birer cümleyle açıklayınız

tail\ --> Düz metin dosyalarının son birkaç satırını görüntülemek için kullanılır.
cat\ --> Bu komutu kullanarak yeni dosyalar yaratabilir, dosyaları açabilir ve taşıyabilir.
sudo\ --> Sıradan kullanıcıların, sisteme yönetici olarak bağlanmaları gerekmeden yönetici yetkisi gerektiren işlemleri yapabilmesini sağlar.
touch\ --> Var olan dosyanın zaman damgasını değiştirir, dosya yoksa yeni bir boş dosya oluşturur.
mkdir --> Yeni dizin ya da dizinler oluşturmak için kullanılır.

## OBJECT ORIENTED PROGRAMMING (60 puan)
-	Taşıtlarla ilgili bir sınıf oluşturulmalıdır. Oluşturulan bu sınıfta aşağıdaki öznitelikler bulunmalıdır.
plakaNo, marka, model, tekerlekSayisi, kanatAcikligi
-	Taşıtılara alternatif olarak üç tane sınıf oluşturulmalıdır:
araba, motorsiklet, uçak
-	Oluşturulan bu sınıflara yukarıda tanımlanan öznitelikler (property) değer olarak girilmeli, aşağıdaki gibi ekrana bastırabilmelidir:

Araba taşıtına ait öznitelikler şu şekildedir:
- Plaka No: 06 ARAC 06
- Marka: Mercedes
- Model: C180
- Tekerlek Sayısı: 4

Motorsiklet taşıtına ait öznitelikler şu şekildedir:
- Plaka No: 06 MOTOR 06
- Marka: Honda
- Model: Forza 750
- Tekerlek Sayısı: 2

Uçak taşıtına ait öznitelikler şu şekildedir:
- Marka: Airbus
- Model: A380
- Kanat Açıklığı: 80m

Yukarıda verilen değerler örnektir. Değerler her taşıt için rastgele girilebilir.

KOD: 
<?php
class Vehicle {
  public $plate;
  public $brand;
  public $model;
  public $wheels;
  public $wing;
  public function __construct($plate, $brand, $model, $wheels, $wing) {
    $this->plate = $plate;
    $this->brand = $brand;
    $this->model = $model;
    $this->wheels = $wheels;
    $this->wing = $wing;
  }
  protected function intro() {
    echo "Plate No: {$this->plate} <br> Brand: {$this->brand} <br> Model: {$this->model} <br> Wheels: {$this->wheels} <br><br>"; 
  }
  protected function introPlane() {
    echo "Brand: {$this->brand} <br> Model: {$this->model} <br> Wing: {$this->wing} <br>"; 
  }
}
class Car extends Vehicle {
  public function message() {
    echo "The attributes of the car vehicle are as follows:<br>";
    $this -> intro();
  }
}
 class Motorcycle extends Vehicle {
  public function message() {
    echo "The attributes of the motorcycle vehicle are as follows:<br>";
    $this -> intro();
  }
}
class Plane extends Vehicle {
  public function message2() {
    echo "The attributes of the plane vehicle are as follows:<br>";
    $this -> introPlane();
  }
}
$car = new Car("34 TC 34", "Mercedes", "AMG G63", "4", "");
$car->message();
$motorcycle = new Motorcycle("34 TC 34", "Honda", "Forza 75", "2", "");
$motorcycle->message();
$plane = new Plane("", "Airbus", "A380","","80m");
$plane->message2();
?>
