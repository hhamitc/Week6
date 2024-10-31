# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği

**1. film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

```sql
  select round(avg(rental_rate),2) from film ;
```

**2. film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

```sql
   select Count(title)from film where title ~~* 'C%';
   select Count(title)from film where title ILIKE 'C%';
  ```

**3. film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

```sql
  select Max(length) from film where rental_rate = 0.99;
   ```

**4. film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

```sql
  select Count(distinct(replacement_cost)) from film where length > 150;
   ```



