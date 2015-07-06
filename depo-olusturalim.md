# Depo (Repository) Oluşturalım

Bu ders en önemli Git komutlarından bazıları hakkında bilgiler içermektedir. İlk önce 
versiyon kontrollü bir projeye başlamak için yapılması gereken ilk iş olan repository 
oluşturma kısmından bahsedilecek. Daha sonraki kısımlarda ise günlük olarak kullanılan 
git komutları anlatılacak.

Bu dersin sonunda yeni bir git destekli bir proje oluşturabilecek, mevcut projenin anlık 
kopyasını alabilecek ve proje üzerinde ne gibi değişiklikler yapıldığını görebileceksiniz.

## git init

```git init``` komutu ile yeni bir Git deposu oluşturulur. Henüz git versiyonlama aktif edilmemiş 
bir proje için ya da henüz başlangıç yapılmamış yeni bir proje için bu komut ile versiyonlamayı 
aktif hale getirebilirsiniz. Bu komut haricindeki diğer Git komutları genel olarak bu komuttan 
sonra kullanılabilir olacatır. Bu nedenle yeni bir projede ilk çalıştırılacak komut da budur.

```git init``` komutu çalıştırılan dizinde ```.git``` isminde yeni bir dizin oluşturur. Bu dizin 
içinde git deposu için gerekli tüm bilgiler bulunmaktadır. Bu bilgilere genel olarak ```metadata``` 
denmektedir. SVN gibi projedeki her klasörün içine revizyon bilgileri tutmak için klasör ya da dosya 
oluşturmaz. Projenin kök dizinine sadece bir adet dizin oluşturur. Bu şekilde projenin içi genel olara 
kirlenmemiş olur. (Daha önce SVN kullananlar ve ilk kez Git öğrenenler için önemli bir ayrıntıdır.)

### Kullanımı

```
git init
```

Çalıştırıldığı dizini Git deposuna çevirecektir. Bu komut çalıştırılan dizine ```.git``` adında bir 
klasör oluşturacaktır. Bu komut ile birlikte proje üzerinde yapılacak değişiklikler kaydedilmeye hazır 
demektir.

```
git init <dizin>
```

Bu komut ```dizin``` adında bir klasör oluşturur ve klasörün içini de git deposuna çevirir.

```
git init --bare <dizin>
```

- [ ] yapılacak

### Tartışma

SVN ile karşılaştırıldığında ```git init``` komutu ile versiyon kontrollü projeler oluşturmak 
son derece kolaydır. Git, bir depo oluşturmanıza, dosyaları içeri aktarmanıza ya da mevcut bir depoyu 
kopyalamanıza gerek duymaz. Tek yapmanız gereken ```cd``` komutuyla dizinin içine girmeniz ve 
```git init``` komutunu çalıştırmanız. Böylece Git deponuz hazır hale gelecektir.

Çoğu projede ```git init``` komutu merkezi bir depo oluşturulurken kullanılır ve geliştiriciler 
kendi bilgisayarlarında ```git clone``` komutunu kullanırlar. Böylece merkezi depoda yer alan projeyi 
kendi bilgisayarlarına almış olur ve Git deposu kullanıma hazır olacaktır.

#### Bare (yalın, çıplak) Depoları

```--bare``` işareti ile  Git deposu oluşturulur ancak çalışma dizini yer almaz. Bu gibi depolarda 
dosyaları düzenlemek ya da değişiklikleri commit etmek mümkün değildir. Merkez Git depoları yalın 
depo olarak oluşturulmalıdır. Çünkü yalın olmayan bir depoya dalları göndermek değişiklikerin üzerine 
yazılmasını sağlayabilir. Şu şekilde de düşünebiliriz. Eğer bir depo ```--bare``` işareti ile oluşturulduysa 
bu depo kodların sadece saklandığı ve üzerinde geliştirme yapılmadığı bir depo olarak düşünülebilir. 
Böylece merkezi depoya yalın depo, diğer geliştiricilerin depolarına  da yalın olmayan depolar debilebilir.

![Yalın ve Yalın Olmayan Depolar](https://cdn.rawgit.com/irfanevrens/gitdersleri/master/resimler/baslangic-rehberi/depo-olusturalim/01.svg)
