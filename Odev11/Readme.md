# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

**1.actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
```sql
 (select first_name from actor) union (select first_name from customer);
```

**2.actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

```sql
 (select first_name from actor) intersect (select first_name from customer)
  ```

**3.actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım. 

```sql
   (select first_name from actor) except (select first_name from customer)
   ```
   
**4.İlk 3 sorguyu tekrar eden veriler için de yapalım.

```sql
    (select first_name from actor) union all (select first_name from customer);
    (select first_name from actor) intersect all (select first_name from customer)
    (select first_name from actor) except all (select first_name from customer)
   ```

