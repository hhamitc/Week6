# Patika+ BackEnd Web Geliştirme Kursu 6. Hafta - SQL Sorgu Örneği

**1.test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

```sql
  create table employee (id int, name varchar(50), birthday DATE, email varchar(100));
```

**2.Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

Örnek olarak 1 adet ekleme sorgusu:
```sql
   insert into employee (id, first_name, email, birthday) values (1, 'Heddi', 'hblondel0@theatlantic.com', '1991/10/18');
  ```

**3.Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

```sql
    update employee set email = 'null' where name like 'B%'returning *;
    update employee set birthday = '1991-01-01' where id = 15 returning *;
    update employee set name = 'mutlu yıllar' where name like 'C%' returning *;
    update employee set birthday ='01.01.2024' where email ilike 'D%' returning *;
    update employee set name ='Hamit' where id=2 returning *;
   ```

**4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

```sql
    delete from employee where email ='null' returning *; 
    delete from employee where name like 'D%' returning *; 
    delete from employee where name ilike '%yıl%' returning *; 
    delete from employee where id between 25 and 30 returning *; 
    delete from employee where birthday between '2003-01-01' and '2004-01-01' returning *; 
   ```




