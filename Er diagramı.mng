# Varlıklar (Entities)

    Yemek (Food)
    Malzeme (Ingredient) 
    Depo (Storage)
    Stok (Stock)

# Öznitelikler (Attributes)

    Yemek: Yemek_ID (PK), Ad, Kategori, Ortalama Gramaj
    Malzeme: Malzeme_ID (PK), Ad, Birim, Kalori
    Depo: Depo_ID (PK), Konum, Kapasite, Depo Türü
    Stok: Stok_ID (PK), Malzeme_ID (FK), Depo_ID (FK), Miktar, Son Kullanma Tarihi
    Yemek Tarifi: Tarif_ID (PK), Yemek_ID (FK), Malzeme_ID (FK), Kullanılan Gramaj

# İlişkiler (Relationships)

    Yemek Tarifi: "Yemek" ile "Malzeme" arasında M:N
    Stok: "Malzeme" ile "Depo" arasında M:1
    Depo-Stok: "Depo" ile "Stok" arasında 1:M
![Image](https://github.com/user-attachments/assets/5e7e3c01-323e-423a-a2d1-c3a04dec5daa)
