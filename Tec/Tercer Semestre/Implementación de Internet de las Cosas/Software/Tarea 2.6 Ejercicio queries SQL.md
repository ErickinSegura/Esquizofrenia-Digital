---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
links: [[Implementación de Internet de las Cosas]]
Fecha: Lunes 06/Noviembre/2023, 04:33 pm


Especificar y ejecutar las siguientes consultas en SQL : 

1. Hacer una consulta para obtener la cardinalidad de la tabla videos, renombrando la columna con el nombre de “Cardinalidad”. 
```sql
SELECT COUNT(*) AS Cardinalidad FROM videos;
```

3. Hacer una consulta que regrese el nombre de los clientes ( member) ordenados por fName y lname. 

```sql
SELECT fName, lname FROM member ORDER BY fName, lName;
```

4. Hacer una consulta que regrese el título del video y su correspondiente director. 

```sql
SELECT v.[title], d.[DirectorName] from Video v, Director d WHERE v.DirectorNo = d.DirectorNo
```

5. Hacer una consulta que regrese el título de video y la cantidad de copias.  

```sql
SELECT v.title, vr.available FROM Video v, VideoForRent fr WHERE v.CatalogNo = vr.CatalogNo
```

6. Hacer una consulta que regrese la cantidad de títulos por categoría ordenado por categoría.  

```sql
SELECT category, COUNT(*) AS Titulos FROM Video GROUP BY category ORDER BY category;
```
 
7. Hacer una consulta que regrese los títulos de las películas cuya renta diaria sea la más cara  

```sql
SELECT title FROM Video WHERE dailyRental = (SELECT MAX(dailyRental) FROM Video);
```

8. Hacer una consulta que regrese los títulos de las películas y lo obtenido por concepto de renta.  

```sql
SELECT V.title, SUM(V.dailyRental) AS Renta FROM Video V INNER JOIN RentalAgreement RA ON V.catalogNo = RA.videoNo GROUP BY V.title;
```

9. Hacer una consulta que regrese los clientes ( member) que actualmente tienen algún video sin entregar.  

```sql
SELECT M.fName, M.lName FROM Member M INNER JOIN RentalAgreement RA ON M.memberNo = RA.memberNo WHERE RA.dateReturn IS NULL;
```

10. Hacer una consulta que regrese el título de la película más rentada.  

```sql
SELECT videoNo FROM RentalAgreement GROUP BY videoNo ORDER BY COUNT(videoNo) DESC LIMIT 1;
```

11. Hacer una consulta que regrese los clientes ( member) que cumplen años en la fecha actual del sistema.  

```sql
SELECT fName, lName FROM Member WHERE MONTH(DOB) = MONTH(CURDATE()) AND DAY(DOB) = DAY(CURDATE());
```

12. Hacer una consulta que regrese los videos que no han sido vistos por ningún cliente   

```sql
SELECT title FROM Video WHERE catalogNo NOT IN (SELECT DISTINCT videoNo FROM RentalAgreement);
```

13. Hacer una consulta que regrese los clientes ( member) que nacieron el mismo año que Lorna  Smith, sin incluirla en el resultado. 

```sql
SELECT M.fName, M.lName FROM Member M WHERE YEAR(M.DOB) = (SELECT YEAR(DOB) FROM Member WHERE fName = 'Lorna' AND lName = 'Smith') AND NOT (M.fName = 'Lorna' AND M.lName = 'Smith');
```


