**Welcome to my Khan Academy SQL Projects. This repository contains my SQL code for all the Khan Academy SQL projects that I have completed.**

/* date created: august 11th 2023
created by: Abhiraj SIngh Dadiyan
description: creating first database project for sql practise, using made up prices for a book store*/

/* create a book store database */
```
create table book_store (
     product_id integer primary key
    ,product_name text
    ,product_price integer not null
    ,quantity integer
    ,rating integer
    ,copies_sold integer);
    
insert into book_store
values
     (1,'A Song of Ice and Fire: Game of Thrones',10.00,50,5,400)
    ,(2,'The Wheel of Time:The Eye of The World',9.00,20,4,100)
    ,(3,'Dune',6.00,25,5,900)
    ,(4,'Sacred Games',8.00,15,4.5,230)
    ,(5,'Stars Need Counting: Essays on Suicide',4.00,20,3.2,90)
    ,(6,'Fallhorne: The World is Burning',9.00,80,3,70)
    ,(7,'Blaze Island',2.99,90,4,10)
    ,(8,'Red Earth and Pouring Rain',19.99,40,4,1000)
    ,(9,'Harry Potter and the Philosopher's Stone',1.99,0,5,17980)
    ,(10,'Shiva Trilogy: The Immortals of Meluha',9.99,150,3,10)
    ,(11,'Percy Jackson and the Olympians: The Lightning Theif',5.55,90,4,15)
    ,(12,'God Emperor of Dune',7.99,23,3.5,10)
    ,(13,'Reverance Trilogy:The Boy with Fire',80.00,18,4,12)
    ,(14,'American Gods',56.00,0,4,5)
    ,(15,'Grown up Digital',7.99,2,3,28);
```
/* display the database ordered by price */
```
select
    *
from
    book_store
order by
    product_price;
```
/* what is the avg rating of the books? */
```
select
    avg(rating)
from
    book_store;
```
/* what are the books we need to restock for the upcoming bookfest? (anything below 50 needs to be restocked) */
```
select
    *
from
    book_store
where
    quantity< 50 
order by
    product_price desc;
```
