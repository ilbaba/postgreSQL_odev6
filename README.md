# postgreSQL_odev6
PostgreSQL -  Altıncı ödev - Ilgar Babashli

# _Q1_ 
film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

# _Ans_
SELECT ROUND (AVG (rental_rate), 3) from film;

Çıktı:
2.980


# _Q2_ 
film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
# _Ans_
SELECT COUNT (*) from film
WHERE title LIKE ('C%');

Çıktı:
92

# _Q3_ 
film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
# _Ans_
SELECT MAX (length) from film
WHERE rental_rate = 0.99;

Çıktı:
0.99

# _Q4_ 
film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
# _Ans_
SELECT COUNT (DISTINCT replacement_cost) FROM film
WHERE length > 150; 

Çıktı:
21
