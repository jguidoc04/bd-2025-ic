# Práctica de Consultas SQL Avanzadas con Northwind (PostgreSQL)

Esta práctica está diseñada para ejercitar habilidades avanzadas en SQL usando la base de datos Northwind. Se trabaja con subconsultas, funciones de ventana, CTEs, vistas, triggers y funciones definidas por el usuario.

---

##  1. Consultas básicas

1. **Lista de productos**  
   Muestra el nombre y el precio unitario de todos los productos disponibles en la base de datos.

2. **Pedidos con país del cliente**  
   Muestra el identificador del pedido, la fecha del pedido y el país del cliente que realizó dicho pedido.

3. **Total de productos vendidos por pedido**  
   Muestra la cantidad total de productos vendidos en cada pedido, sumando todas las unidades por pedido.

---

##  2. Subconsultas

4. **Productos con precio superior al promedio**  
   Lista los nombres y precios de los productos cuyo precio unitario sea superior al precio promedio de todos los productos.

5. **Clientes sin pedidos recientes**  
   Muestra todos los clientes que no han realizado pedidos en los últimos 6 meses.

6. **Pedidos con ventas superiores al promedio**  
   Muestra los pedidos cuyo monto total vendido (cantidad × precio) supera el promedio de ventas de todos los pedidos.

---

##  3. CTE (Common Table Expressions)

7. **Total de ventas por producto**  
   Utilizando un CTE, calcula el total vendido por cada producto (multiplicando cantidad por precio unitario), y luego muestra el nombre del producto y el total vendido.

8. **Top 3 empleados por pedidos por trimestre**  
   Usa un CTE para calcular cuántos pedidos ha procesado cada empleado por trimestre, y muestra el top 3 de empleados más activos por ese período.

---

##  4. CTE recursivos

9. **Jerarquía de empleados**  
   Asumiendo que existe una relación de dependencia entre empleados (empleado-reporta_a), usa un CTE recursivo para listar toda la jerarquía desde los jefes hasta los subordinados, indicando el nivel jerárquico.

---

##  5. Vistas

10. **Ventas por categoría de productos**  
    Crea una vista que muestre el nombre de cada categoría y el total vendido de todos sus productos (cantidad × precio).

11. **Resumen de clientes**  
    Crea una vista que muestre el identificador del cliente, su nombre, la cantidad total de pedidos realizados y el monto total comprado.

12. **Ventas por país**  
    Crea una vista que relacione los países de los clientes con el total vendido en cada uno.

---

##  6. Triggers

13. **Auditoría de cambios en productos**  
    Crea una tabla de auditoría y un trigger que registre cualquier inserción, actualización o eliminación sobre la tabla `products`, guardando la acción y el identificador del producto afectado.

14. **Validación de precios negativos**  
    Crea un trigger que evite que se inserten o actualicen productos con precios negativos en la tabla `products`.

15. **Auditoría de pedidos eliminados**  
    Crea un trigger que registre en una tabla de auditoría todos los pedidos que sean eliminados, guardando su ID y fecha.

---

##  7. Funciones definidas por el usuario

16. **Total vendido por pedido (función)**  
    Crea una función que reciba el identificador de un pedido y devuelva el total vendido (suma de cantidad × precio de cada producto en ese pedido).

17. **Promedio de compra por cliente (función)**  
    Crea una función que, dado el identificador de un cliente, devuelva el promedio del monto total comprado por cada pedido que haya realizado.

---

##  8. Consultas complejas con funciones de ventana

18. **Producto más vendido por categoría**  
    Usa funciones de ventana para encontrar el producto más vendido (por cantidad) en cada categoría.

19. **Empleado con más ventas**  
    Muestra el nombre del empleado que ha vendido el mayor monto total (cantidad × precio) sumando todos los pedidos que haya atendido.

20. **Tres productos menos vendidos**  
    Muestra los 3 productos menos vendidos de toda la base de datos, ordenados de menor a mayor por cantidad total vendida.

---

