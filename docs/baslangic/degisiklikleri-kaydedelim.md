# Değişiklikleri Kaydedelim

![Değişiklikleri Kaydedelim](https://www.atlassian.com/git/images/tutorials/getting-started/saving-changes/hero.svg)

## git add

Bu komut depodaki bir değişikliği Geçiş Bölgesi'ne (Staging Area) ekler. Bir sonraki commit'de hangi dosyalarda değişiklikler olduğunu belirtir. Bununla beraber ```git add``` komutunun depo üzerinde bir etkisi olmaz. Yapılan değişiklikler depo içine ancak ```git commit``` komutu ile dahil edilebilir. Bu nedenle ```git add``` komutu ile eklenen dosyalar Geçiş Bölgesi'ne alınır.

Bu komutlar ile birlikte ```git status``` komutu da kullanılmaktadır. Bu komut ile de çalıştığımız deponun ve Geçiş Bölgesi'nin genel durumuna bakılabilir.
 
### Kullanımı

```
git add <dosya>
```

Bir sonraki committe kaydedilmek üzere ```<dosya>``` içindeki değişiklikleri Geçiş Bölgesi'ne ekler.

```
git add <dizin>
```

Bir sonraki committe kaydedilmek üzere ```<dizin>``` içindeki değişiklikleri Geçiş Bölgesi'ne ekler.

```
git add -p
```

Bu komut ile interaktif olarak Geçici Bölge süreci başlatılır. Üzerinde değişiklik yapılmış dosyalar için ne yapmak istediğinizi sorar. Cevap olarak;
 
  * ```y``` - Geçiş Bölgesi'ne göndermek için 
  * ```n``` - Gözardı etmek için
  * ```q``` - Gözardı et ve kalan değişiklikler için işlem yapmadan süreci bitir.
  * ```a``` - Geçiş Bölgesi'ne gönder ve kalan değişiklikler için de aynısını yap.
  * ```d``` - Dosya bazlı olarak mevcut değişikliği kalan değişiklikleri gözardı et.

### Tartışma

```git add``` ve ```git commit``` komutları Git iş akışının temellerini oluşturmaktadır. Bu iki komut Git'i kullanmak isteyen herkes tarafından, ekip ya da bireysel olsun, iyi anlaşılması gerekir. Bu komutların yaptığı iş kısaca depo için versiyon geçmişlerini oluşturmak ve bunları kayıt altına almaktır.

Bir proje üzerinde çalışmak genel olarak düzenle/geçiş bölgesine gönder/commit yap şeklindedir. Öncelikle üzerinde değişiklik yapılması gereken dosyalar üzerinde gerekli değişiklikler yapılır. Yapılacak değişiklikler tamamlandıysa yapılan değişiklikler ```git add``` komutu ile Geçiş Bölgesi'ne gönderilir. Daha sonra Geçiş Bölgesi'ndeki mevcut durumdan memnunsanız, yani herhangi bir aksaklık ya da eksiklik yoksa proje üzerinde yapılan değişiklikleri proje geçmişine yazılmak üzere ```git commit``` komutu kullanılır.

![Değişiklikleri Kaydedelim](https://www.atlassian.com/git/images/tutorials/getting-started/saving-changes/01.svg)