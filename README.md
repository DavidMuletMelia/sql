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
