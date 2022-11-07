# sql
SQL introduction for the unit

select AVG(price) from products; // sacar la media de la columan

SELECT MAX(price) FROM products;


INSERT INTO products

min max avg sum (no se puede acompañar con nada mas, no podemos poenr el min o max y quien lo tiene, pero si con group by)


como sacar el minimo

Select ProductName FROM Products WHERE Price = (Select min(PRODUCT) FROM products)

Select ProductName 
FROM Products 
WHERE Price = (Select min(price) FROM products);

que trabajadores son los que tienen el salario mayor que la media de salarios
que productos son los que tienen el precio mayor que la media
cual es la suma de los precios de los productos
que producto(s) tienen el minimo precio
que productos tienen el precio maximo

es posible tener un valor igual que la suma, si todos suman 0 o si hay valores negativos y positivos


Select ProductName as nombre_producto, price as precio_producto
FROM Products
WHERE Price > (Select avg(price) FROM products)
order by precio_producto asc;


Obtener los nomrbes de los productos de la tienda y el precio
SELECT Name, Price
FROM Articulos

Obtener los nomrbes de los productos de la tienda de los que el precio sea mayor o igual a 200
SELECT Name
FROM Articulos
WHERE Price ≥ '200';

SELECT *
FROM Articulos
WHERE Price = BETWEEN 60 AND 120;


Obtener los precios de los productos y el precio de estos en pesetas (multiplicado por 166.88)
SELECT Name, Price *166.88
FROM Articulos; (no del todo bien)

SELECT Name, Price *166.88 AS Pesetas
FROM Articulos;
 (ahora ya si bien)

Selecciona el precio medio de los productos
SELECT AVG(Price)
FROM Articulos

Obtener el precio medio de los articulos cuyo codigo de fabricante sea 2
SELECT AVG(Price)
FROM Articulos
WHERE Codigo = 2;

Obtener el numero de articulos cuyo precio sea mayor o igual que 180
SELECT Count(*) AS Num_Articulos
FROM Article
WHERE Price >= 180;

Nombre y precio articulos cuyo precio sea mayor o igual a 180 ordenar desc por precio y por nombre
SELECT Name, Price
FROM Article
WHERE Price >= 180;
ORDER BY Price DESC AND Name ASC;
