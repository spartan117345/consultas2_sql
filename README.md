# consultas2_sql

base de datos empresa 

![BD-empresa](img/Empresa.jpg)


# empleados

![listado_empleados](img/empleados.png)

# departamentos

![listado_departamentos](img/departamentos.png)

# apellidos de los empleados


`SELECT apellidos_empleado FROM Empleado;`


![apellidos_de los_empleados](img/empleados_apellidos.png)

# apellidos de los empleados sin repeticion 


`SELECT DISTINCT apellidos_empleado FROM Empleado;`


![apellidos_de los_empleados](img/apellidos_empleados.png)

# los empleados que se apelliden gomez

`SELECT * FROM Empleado WHERE apellidos_empleado = 'Gomez';`

![apellidos_gomez](img/apellido_gomez.png)

# los empleados con los apellidos dias y rodrigues 

` SELECT *
FROM Empleado WHERE apellidos_empleado LIKE 'Diaz%' OR apellidos_empleado LIKE 'Rodriguez%'; `

![apellidos_diaz_rodrigues](img/apellido_diaz_rodriguez.png)


# Obtener los nombres de los empleados que trabajan en el departamento 11


` SELECT nombre_empleado FROM Empleado WHERE id_departamento = 11; `

![departamento_11](img/departamento11.png)

# listado de los empleados que tengan un apellido que empiece por s

SELECT * FROM Empleado WHERE apellidos_empleado LIKE 'S%';

![apellido_s](img/apellido_p.png)


# presupuesto total de los departamentos

`SELECT SUM(presupuesto_departamento) AS presupuesto_total FROM Departamento;`


![presupuesto](img/presupuesto.png)


# numero de empleados de cada departamento

`SELECT id_departamento, COUNT(*) AS numero_empleados FROM Empleado GROUP BY id_departamento`

![personal_departamento](img/personal_departamento.png)

# los datos de cada empleado con los datos de su departamento

`SELECT * FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento;`

![empleado_datos_departamentp](img/empleado_datos_departamento.jpg)

# los datos de los empleados junto con el presupuesto de su departamento

`SELECT e.nombre_empleado, e.apellidos_empleado, d.nombre_departamento, d.presupuesto_departamento FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento;`

![empleado_presupuesto](img/empleado_presupuesto.png)

# los empleados cuyo departamento tenga un presupuesto mayor a 10000000

`SELECT e.nombre_empleado, e.apellidos_empleado FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento WHERE d.presupuesto_departamento > 100000000;`

![empleado_presupuesto2](img/apellido_diaz_rodriguez.png)
