# Apuntes del curso de sql server Query 2012 


## Guid 
El guid es un identificado único que se utiliza en muchas ocasiones con llave primaria de un registro 
Ej:

```sh
 DECLARE @UNI UNIQUEIDENTIFIER
SET @UNI = NEWID()
 
SELECT @UNI
  ```


#Declarar variables temporales

Esto lo podemos utilizar para almacenar un tipo de dato en un puntero o espacio en momoria que podríamos utilizar como ancla en un futuro 
Ej:

```sh
DECLARE @find VARCHAR(30);   
/* Also allowed:   
DECLARE @find VARCHAR(30) = 'Man%';   
*/  
SET @find = 'Man%';   
SELECT p.LastName, p.FirstName, ph.PhoneNumber  
FROM Person.Person AS p   
JOIN Person.PersonPhone AS ph ON p.BusinessEntityID = ph.BusinessEntityID  
WHERE LastName LIKE @find; 
  ```
