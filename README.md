# Apuntes del curso de sql server Query 2012 


## Guid 
El guid es un identificado único que se utiliza en muchas ocasiones con llave primaria de un registro 
Ej:

```sh
 DECLARE @UNI UNIQUEIDENTIFIER
SET @UNI = NEWID()
 
SELECT @UNI
  ```


## Declarar variables temporales

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
  
  
  # Funciones para manejar cadenas de caracteres


  ## LEFT
  Puede utilizar la siguiente plantilla para extraer caracteres de la 
 
  ```sh
 SELECT  
LEFT(identifier,5) AS identifier
FROM TestDB.dbo.table_1
  ```
  
  ## STUFF
  Elimina 3 caracteres de una cadena, comenzando en la posición 1, y luego inserte "HTML" en la posición 1:


   ```sh
SELECT STUFF('SQL Tutorial', 1, 3, 'HTML');
  ```
  
  
  ## SUBSTRING
  
  SUBSTRING () extrae una subcadena con una longitud especificada a partir de una ubicación en una cadena de entrada.
   ```sh
SELECT SUBSTRING('SQL Tutorial', 1, 3) AS ExtractString; 
```

## STR
Retorna un numero como string

   ```sh
SELECT STR(185);
```
  
   
   
  
  
  
  
