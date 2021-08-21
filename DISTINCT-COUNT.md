## DISTINCT-COUNT Komut kullanım örenkleri
---

1. film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

![sorgu1](img/dıstınct1.jpg)

```SQL
SELECT DISTINCT replacement_cost FROM film;
```

2. film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?

![sorgu2](img/dıstınct2.jpg)

```SQL
SELECT COUNT (DISTINCT replacement_cost) FROM film 

```

3. film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

![sorgu3](img/dıstınct3.jpg)

```SQL
SELECT COUNT (title)  FROM film 
WHERE title LIKE 'T%' AND rating = 'G';
```

4. country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?


![sorgu4](img/dıstınct4.jpg)

```SQL
SELECT COUNT (country LIKE'_____')  FROM country;
```

5. city tablosundaki şehir isimlerinin kaçtanesi 'R' veya r karakteri ile biter?


![sorgu5](img/dıstınct5.jpg)

```SQL
SELECT COUNT (city ILIKE'%r')  FROM city;
```