# phpmyAdmin
Avance de nuevos ejemplos en phpmyadmin
# consulta_1_sql
# Introduccion a las consultas a una BD usando el lenguaje SQL

## Base de datos: Ventas
## Tabla: Cliente

![Tabla Cliente](/img/tabla_Cliente.png "Tabla Cliente")

## Instruccion SELECT
- permite seleccionar datos de una tabla
- su formto es: `SELECT campos_tabla FROM nombre tabla``

### consulta No. 1 
1. para visualizar toda la informacion que contiene la tabla cliente se puede incluir con la instruccio SELECT el caracter **\*** caa uno de los campos de la tabla.

- `SELECT * FROM Cliente`
![Tabla Cliente](./img/ejem1.png "Tabla Cliente")

- `SELECT identificacion, nombre, apellidos, 
direccion, telefono, ciudad_nac, fecha_nac FROM Cliente`
![Tabla Cliente](./img/ejem2.png "Tabla Cliente")

### consulta No. 2

2. para visualizar solamente la identificacion del cliente:`SELECT identificacion FROM Cliente`
![Tabla Cliente](./img/ejem3.png "Tabla Cliente")

### consulta No. 3

3. si se desea obtener los registros cuya identificacion sea mayor o igual a 150, se debe utilizar la cláusula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * FROM Cliente Where identificacion>=150`


![Consulta3](./img/consulta3.png "Consulta 3")

### Consulta No. 4

4.  Se desea obtener los registros cuyos apellidos sean vanegas o cetina, se deba utilizar el operador `IN` que especifica los registros que se quieren visualizar de una tabla. 

SELECT apellidos, nombre FROM `cliente` WHERE apellidos IN('Vanegas', 'Cetina');
![Consulta4_1](./img/consulta4_1.png "Consulta 4_1")


o se puede utilizar el operador `OR`

`SELECT apellidos FROM cliente WHERE apellidos = 'Vanegas'OR apellidos = 'Cetina'`
![Consulta4_2](./img/consulta4_2.png "Consulta 4_2")


### Consulta No. 5

5. Se desea obtener los registros cuya identificación sea menor de 110 y la ciudad sea cali, se debe utilizar el operador `AND`

`SELECT * FROM cliente WHERE identificacion<=110 AND ciudad = 'Cali'`
![Consulta5](./img/consulta5.png "Consulta 5")



### Consulta No. 6

6. Si desea obtener los registros cuyos nombres empiecen por la letra 'A' , se debe utilizar el operador `LIKE` que utiliza los patrones `%` (Todos) y `_`(caracter)

`SELECT * FROM `cliente` WHERE nombre LIKE 'A%'`
![Consulta6](./img/consulta6.png "Consulta 6")

### Consulta No. 7

7. Se desea obtener los registros cuyos nombres contengan la letra 'a'

`SELECT * FROM `cliente` WHERE nombre LIKE '%a%'`

![Consulta7](./img/consulta7.png "Consulta 7")

### Consulta No. 8

8. Se desea obtener los registros donde la cuarta letra del nombre del cliente sea la letra 'a'

`SELECT * FROM `cliente` WHERE nombre LIKE '___a'`

![Consulta8](./img/consulta8.png "Consulta 8")

### Consulta No. 9 

9. Si se desea T los registros cuya identificacion esté entre el intervalo 110 y 150, se debe utilizar la cláusula `BETWEEN`, que sirve para especificar un intervalo de valores.

`SELECT * FROM cliente WHERE identificacion BETWEEN 110 AND 150`

![Consulta9](./img/consulta9.png "Consulta 9")


## Instrucción DELETE
- Permite borrar todos o un grupo especifico de registros de una tabla.
- Su formato es: `DELETE FROM nombre_tabla`

### Eliminación No. 1

1.  Eliminar los registros cuya identificación sea mayor a 150 

`DELETE FROM `cliente` WHERE identificacion > 170`

![ConsultaEli1](./img/consultaEli1.png "ConsultaEli 1")

2. Eliminar los registros cuya identificacion sea igual a 116

`DELETE FROM cliente WHERE identificacion =116`

![ConsultaEli2](./img/consultaEli2.png "ConsultaEli 2")

![ConsultaEli2-1](./img/consultaEli2-1.png "ConsultaEli 2-1")

## Instrucción UPDATE
- Permite actualizar un campo de tabla 
- Su formato es: `UPDAYE nombre_tabla SET nombre campo = valor`

### Actualización  No. 1
1. Para actualizar la ciudad de nacimiento Cristian vanegas, cuya Identificación es 114 

`UPDATE cliente SET ciudad_nac = 'Pereira' WHERE identificacion = 114`

![Actualizacion1](./img/actualizacion1.png "actualizacion 1")

![Actualizacion](./img/actualizacion1-1.png "actualizacion 1-1")
