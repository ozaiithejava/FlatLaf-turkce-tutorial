# [FLATLAF](https://www.formdev.com/flatlaf/) Türkce tutorial
türkiyede ilk flatlaf tutorial
[FLATLAF](https://www.formdev.com/flatlaf/)
### İlk adım kurulum

1-öncelikle javanın güncel bir versiyonunu indiriniz. (18 ideal)

2-IntelliJ IDEA yı acın

3-maven projecsi oluşturun

4-pom.xml e sunu yapıstırın
```
 <dependencies>
   
        <dependency>
        
            <groupId>com.formdev</groupId>
            
            <artifactId>flatlaf</artifactId>
            
            <version>3.1.1</version>
            
        </dependency>
        
    </dependencies>
```

boylece lib i eklemiş olduk

5-main sınıfımızı oluşturup try-catch bloğunun içerisine 

**UIManager.setLookAndFeel( new FlatDarkLaf() );**
kodunu yapıştırıyoruz böylece FlatDarkLaf temasını aktif hale getirmiş oluyoruz

Not: Unutmayın bu lib  Swing ile kullanılmakta bir tür tema gibi düşünebilirsiniz

6-  **JFrame frame = new JFrame("FlatLaf Öğretici");**

boylece Jframe yi frame adlı bir objeye yönelttik ve panel ismini FlatLaf Öğretici yapmış olduk 

7-frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

**boylece klasik kapatma tuşuna basınca kapatma işlemini tanımlamış olduk**

8- 
frame.setSize(400, 300);

**frame boyutunu x ve y yi 400 ve 300 olarak ayarlıyoruz (set demek ayarla ata demek)**

frame.setLocationRelativeTo(null);

**penceremiz açılınca ortada başlatmasını sağlıyor**


frame.setVisible(true);

**penceremizin görünür olmasını sağlıyor false yazar isek gorunmez olur**

evet kurulum tamamlandı 

şimdi size basit birkaç kod gösterelim:

JOptionPane.showMessageDialog(null, "Merhaba, Dünya!");;

Bir pencere açar ve Merhaba Dünya! yazar bunu ne gibi yerlerde kullanabiliriz bize uygulama örneği göster 

tabiki işte örnek:
```
public class app  {
    static private int min_age = 18 ;
    private static Scanner sc = new Scanner(System.in);
    public static void main(String[] args) {
        FlatLaf.install(new FlatDarkLaf());
        System.out.println("Yaşınızı giriniz Kafeye girmek için 18 yaş ve üstünde olmalısınız");
        int c = sc.nextInt();
        if (c >= min_age){
            JOptionPane.showMessageDialog(null, "Hoşgeldiniz");;
        }else{
            int result = min_age-c;
            JOptionPane.showMessageDialog(null, result+" kadar sene sonra giriş yapabilirsiniz!");;
        }
    }
}
```
devamı yakında eklenecektir

[discordum](https://discord.gg/5TdaEjFnBW)

