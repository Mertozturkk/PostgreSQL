# PostgreSQL WHERE, AND, OR, NOT sorguları

Bu çalışmada PostgreSQL DBSM kullanarak aritmetik ve mantıksal operatörler yardımı ile Query çalışma örneklerine bakacağız.

Sorgu senaryoları [dvdrental](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip) veritabanı üzerinden gerçekleştirilmiştir.

-----------

1. film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.


![sorgu1](PostgreSQL/img/dvdrental_1.jpg)

```SQL

SELECT title, description FROM film;


```

2. film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.

![sorgu2](PostgreSQL\img\dvdrental_2.jpg)

```SQL
SELECT * FROM film
WHERE length >60 AND length < 75;
```

3. film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.

![sorgu3](PostgreSQL\img\dvdrental_3.jpg)

```SQL
SELECT * FROM film
WHERE  rental_rate = 0.99 AND replacement_cost = 12.99 OR replacement_cost = 28.99;
```

4. customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?

![sorgu4](PostgreSQL\img\dvdrental_4.jpg)

```SQL
SELECT first_name, last_name FROM customer
WHERE  first_name = 'Mary';
```

5. film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.

![sorgu5](PostgreSQL\img\dvdrental_5.jpg)

```SQL
SELECT * FROM film
WHERE  NOT (length > 50 AND rental_rate = 2.99 OR rental_rate = 4.99)
```
