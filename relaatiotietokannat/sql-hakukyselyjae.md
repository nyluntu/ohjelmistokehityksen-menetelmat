---
description: >-
  Sivulle on kerätty harjoituksina tehtyjä kyselyjä. Kaikkia kyselyjä ei ole
  tarkistettu, joten niissä voi olla joitakin virheitä.
---

# SQL hakukyselyjä

## Esimerkkikyselyjä

Kuinka monta kertaa asiakkaat ovat tehneet tilauksia keskimäärin koko tilaushistorian ajalta?

```sql
SELECT customerNumber,
       COUNT(*)
FROM orders
GROUP BY customerNumber;

--kuinka monta kertaa yksittäinen asiakas on tilannut

SELECT customerNumber,
       COUNT(*)
FROM orders
WHERE status = "Shipped"
GROUP BY customerNumber;

--sama mutta näyttää vain ne jotka on shipped

SELECT AVG(d.c) AS keskiarvo
FROM
  (SELECT customerNumber,
          COUNT(*) AS c
   FROM orders
   WHERE status = "Shipped"
   GROUP BY customerNumber)AS d;
```

Päivissä kerrottuna, mikä on toistuvia tilauksia tehneiden asiakkaiden keskimääräinen tilausaika? Ostaako asiakas siis viikoittain, kuukausittain vai vuosittain tuotteita? 

```sql
SELECT customerNumber, (MAX(orderDate) - MIN(orderDate)) / (COUNT(*) – 1
FROM orders
GROUP BY customerNumber
HAVING COUNT(*) > 1;
```

Ketkä ovat asiakkaista ovat kärjessä tilauksien määrän mukaan järjestettynä koko tilaushistorian ajalta?

```sql
SELECT customerNumber,
       COUNT(*)
FROM orders
GROUP BY customerNumber
ORDER BY COUNT(*) DESC
LIMIT 3;
```

Montako tilausriviä tilaukset keskimäärin sisältävät koko tilaushistorian ajalta?

```sql
SELECT count(orderLineNumber) / count(DISTINCT orderNumber) AS orders
FROM orderdetails;
```

Tilauksien kokonaissummaa euroissa tarkasteltuna, mikä on kertaostosten keskimääräinen summa, maksimi ja minimi?

```sql
SELECT MAX(total),
       MIN(total),
       AVG(total)
FROM
  (SELECT orderNumber,
          SUM(quantityOrdered * priceEach) AS total
   FROM orderdetails
   GROUP BY orderNumber) AS x;
```

Mikä on keskimääräinen myynti kuukausittain lähetettyjen myyntien osalta koko tilaushistorian ajalta?

```sql
SELECT MONTH(orderDate) AS MONTH,
       YEAR(orderDate) AS YEAR,
       avg(quantityOrdered * priceEach) AS AVG
FROM orders
INNER JOIN orderdetails USING (orderNumber)
WHERE status = 'shipped'
GROUP BY YEAR,
         MONTH WITH ROLLUP;
```

Mikä on keskimääräinen toimitusaika tilauksen saapumisen ja lähettämisen välillä koko tilaushistorian ajalta?

```sql
SELECT round(avg(datediff(shippedDate, orderDate)))
FROM orders
WHERE status = 'shipped';
```

Ketkä asiakkaista ovat parhaiten maksavia asiakkaita, jotka ovat hoitaneet maksunsa?

```sql
SELECT contactFirstName,
       contactLastName,
       city,
       country,
       amount
FROM customers
INNER JOIN payments
ORDER BY `payments`.`amount` DESC;
```

Ketkä asiakkaista ovat parhaiten tilaavia eli ovat tehneet useimpia tilauksia?

```sql
SELECT contactFirstName,
       contactLastName,
       city,
       country,
       quantityOrdered
FROM customers
INNER JOIN orderdetails
ORDER BY `orderdetails`.`quantityOrdered` DESC;
```

Mitkä tuotteet ovat myyneet parhaiten koko tilaushistorian aikana?

```sql
SELECT productName,
       sum(quantityOrdered)
FROM products
INNER JOIN orderdetails ON products.productCode = orderdetails.productCode
GROUP BY productName
ORDER BY sum(quantityOrdered) DESC
LIMIT 10;
```

Pienoismallin koon mukaan laskettuna, mitkä tuotteista ovat myyneet parhaiten tilaushistorian aikana?

```sql
SELECT productScale,
       sum(quantityOrdered) AS "Total orders",
       sum(quantityOrdered*priceEach) AS "Total sales"
FROM products
INNER JOIN orderdetails ON products.productCode = orderdetails.productCode
GROUP BY productScale
ORDER BY sum(quantityOrdered) DESC;
```

Keskittyen vain muutamaan parhaiten myyvään tuotteeseen niin mihin maihin kyseisiä tuotteita myydään?

```sql
SELECT country,
       city,
       productCode,
       sum(quantityOrdered*priceEach) AS total
FROM orderdetails
INNER JOIN orders ON orderdetails.orderNumber = orders.orderNumber
INNER JOIN customers ON customers.customerNumber = orders.customerNumber
WHERE productCode IN ("S700_4002",
                      "S18_3232",
                      "S18_1342")
GROUP BY country,
         city,
         productCode
ORDER BY `total` DESC;
```

Mitkä tuoteryhmistä ovat parhaiten myyviä koko tilaushistorian aikana?

```sql
SELECT productLine,
       sum(quantityOrdered*priceEach)
FROM products
INNER JOIN orderdetails ON products.productCode = orderdetails.productCode
GROUP BY productLine
ORDER BY sum(quantityOrdered*priceEach) DESC;
```

Ketkä ovat TOP10 huippumyyjää koko tilaushistorian ajalta?

```sql
SELECT salesRepEmployeeNumber,
       firstName,
       lastName,
       officeCode,
       SUM(quantityOrdered * priceEach) sales
FROM customers
INNER JOIN orders USING (customerNumber)
INNER JOIN orderdetails USING (ordernumber)
INNER JOIN employees ON employeeNumber = salesRepEmployeeNumber
INNER JOIN offices USING (officeCode)
GROUP BY salesRepEmployeeNumber
ORDER BY sales DESC
LIMIT 10;
```

Mitkä toimipaikoista ovat parhaiten myyviä niiden myynnin mukaan järjestettynä?

```sql
SELECT officeCode,
       offices.city,
       SUM(quantityOrdered * priceEach) sales
FROM customers
INNER JOIN orders USING (customerNumber)
INNER JOIN orderdetails USING (ordernumber)
INNER JOIN employees ON employeeNumber = salesRepEmployeeNumber
INNER JOIN offices USING (officeCode)
GROUP BY officeCode
ORDER BY sales DESC;
```

