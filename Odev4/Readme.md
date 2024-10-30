# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği

1. **film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

```sql
  select distinct replacement_cost from film;
```

2. **film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?

```sql
   select count(distinct replacement_cost) from film;
   ```

3. **ffilm tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

```sql
   select count(title) from film where title ~~'T%' and rating ='G' ;
   ```

4. **country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?

```sql
   select Count(country) from country where country ~~'_____';
   ```

5. **city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

```sql
   select count(city) from city where city ~~* '%r';
   select count(city) from city where city ILIKE '%r';
   ```