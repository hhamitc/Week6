# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği

**1.film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.

```sql
  select rating, Count(*) from film group by rating;
```

**2.film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

```sql
   select replacement_cost, Count(*) from film group by replacement_cost having count(*) > 50;
  ```

**3.customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?

```sql
  select store_id, Count(*) from customer group by store_id;
--select store_id,Count(store_id) from customer group by store_id;
   ```

**4. film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

```sql
  select Count(distinct(replacement_cost)) from film where length > 150;
   ```

**4.city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

```sql
  select country_id, count(*) from city group by country_id order by count(*) desc limit 1;
   ```


