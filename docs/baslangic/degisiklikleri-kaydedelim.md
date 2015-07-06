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

