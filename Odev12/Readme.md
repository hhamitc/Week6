# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği
Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

**1.film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```sql
   Select Count(*) from film where length > (select avg(length) from film );
```

**2.film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

```sql
 select Count(*) from film where rental_rate = (select max(rental_rate) from film)
  ```

**3.film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

```sql
   select * from film where rental_rate = (select min(rental_rate)from film) and replacement_cost =(select min(replacement_cost)from film);
   ```
   
**4.payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

```sql
   select customer.customer_id, customer.first_name , customer.last_name , sum(amount) 
   from customer 
   join payment on payment.customer_id = customer.customer_id 
   group by customer.customer_id, customer.first_name , customer.last_name 
   order by sum(amount) desc;
   ```

Soruyu yanlış anlamış olma ihtimalime karşı ikinci alternatif;
```sql
   select customer.customer_id, customer.first_name , customer.last_name ,Count(*) 
   from payment
   inner join customer on payment.customer_id = customer.customer_id 
   group by customer.customer_id, customer.first_name , customer.last_name order by Count(*) desc;
   ```



