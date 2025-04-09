## a) Her bir kitabın başlığını ve yılını listeleyiniz.

    π(Başlık, yıl)(kitap)

## b) Bölümü IIS olan öğrencilerin tüm bilgilerini listeleyiniz

    π(*) (σ(bolum = 'IIS')(öğrenci))

## c) Tüm öğrencileri ödünç alabilecekleri kitaplarla listeleyiniz.

    π(öğrenci.ogrADI, kitap.Başlık) (öğrenci ⨝ odunc ⨝ kitap)

## d) SAÜ tarafından 1990 yılından önce yayınlanan tüm kitapları listeleyiniz

    π(Başlık, yıl) (σ(yayıncı = 'SAÜ')(σ(yıl < 1990)(kitap)))

## e) Sakarya’da yaşayan yazarların isimlerini listeleyiniz.

    π(yAdi) (σ(adres = 'Sakarya')(yazar))

## f) 30 yaşından büyük ve IIS de olmayan öğrencilerin adını listeleyiniz.

    π(ogrADI) (σ(yas > 30)(σ(¬(bolum = 'IIS'))(öğrenci)))

## g) YAdi alanını Adi olarak değiştiriniz.

    cebirsel ifadeler sadece veri sorgulamayla çalışır yani isim değiştirme yapamayız bunun için SQL lazım 

## h) IIS de okuyan ve bir kitap ödünç alan tüm öğrencileri listeleyiniz.

    π(öğrenci.ogrADI) (σ(bolum = 'IIS')(öğrenci ⨝ odunc))

## i) ’Ali’ tarafından yazılan kitapların başlıklarını listeleyiniz. (kartezyen)

    π(kitap.Başlık) (σ(yAdi = 'Ali')(yazılmıs ⨝ kitap))

## j) ’Ali’ tarafından yazılan kitapların ‘veritabanı’ anahtarı içermeyen kitapların başlıklarını listeleyiniz.

    π(kitap.Başlık) ((σ(yAdi = 'Ali')(yazılmıs ⨝ kitap ⨝ acıklama)) - (σ(Anahtar = 'veritabanı')(yazılmıs ⨝ kitap ⨝ acıklama)))

## k) Herbir kitabı anahtarlarıyla birlikte listeleyiniz.anahtarı olmayan kitapların listelenmediğine dikkat edin.

    π(kitap.Başlık, acıklama.Anahtar) (kitap ⨝ acıklama)

## l) her öğrenciyi ödünç aldığı kitaplarla bilrikte listeleyiniz.

    π(öğrenci.ogrADI, kitap.Başlık) (öğrenci ⨝ odunc ⨝ kitap)

## m) ’YASİN’ isimli yazarlartarafından yazılan kitapların başlıklarını listeleyiniz.(join)

    π(kitap.Başlık) (σ(yAdi = 'YASİN')(yazılmıs ⨝ kitap))

## n) ’Veli’ isimli öğrencinin ödünç aldığı kitapların yazarlarını listeleyiniz.

    π(yazar.yAdi) (σ(ogrADI = 'Veli')(öğrenci ⨝ odunc ⨝ yazılmıs ⨝ yazar))

## o) Hangi kitaplar ‘veritabanı’ ve ‘programlama’ anahtarlarının her ikisine de sahiptir?

    π(kitap.Başlık) (σ(Anahtar = 'veritabanı')(acıklama ⨝ kitap)) ∩ π(kitap.Başlık) (σ(Anahtar = 'programlama')(acıklama ⨝ kitap))

