1- film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.  
```sh
SELECT ROUND(AVG(rental_rate),3) FROM film;
```
2- film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.  

```sh
SELECT replacement_cost, COUNT(*) FROM film GROUP BY replacement_cost HAVING COUNT(replacement_cost) > 50;
```
3- customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?  

```sh
SELECT store_id, COUNT(*) FROM customer GROUP BY store_id;
```
4- city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

```sh
SELECT country_id, COUNT(country_id) FROM city GROUP BY country_id ORDER BY COUNT(country_id) DESC LIMIT 1;
```
