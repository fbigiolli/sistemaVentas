# Sistema de Ventas

Este proyecto fue realizado en forma de TP grupal durante la cursada de algoritmos y estructuras de datos II, pasando por tres fases:
especificacion, diseño e implementacion. El código que se ve en este repositorio corresponde a la implementación, con sus tests asociados.
En la carpeta src se encuentran varios archivos, tanto cpp como headers. fachada_lollapatuza es una fachada que se implementó por la cátedra con el objetivo de simplificar para ellos el testeo de los TP's. lollapatuza es el modulo correspondiente a un festival (de nombre sospechosamente parecido a uno real), y puesto es el módulo correspondiente a cada uno de los puestos que se registran para vender en el festival. A continuación hay una descripción de las funciones del modulo lollapatuza, y sus complejidades. Varias de estas funciones utilizan funciones del modulo puesto, y ninguna rompe con su encapsulamiento.  

## Tests

Para correr los tests usamos el framework Google Test. Por default el codigo de este repositorio esta configurado para correrlos. Ya se incluyen las librerias necesarias.

## Renombres
- A: Cantidad de personas en el sistema
- I: Cantidad total de items en todo el festival
- P: Cantidad de puestos
- cant: Cantidad total de descuentos disponibles para dicho item.


## lollapatuza
O(A * I + P * I). Inicializa una instancia nueva de lollapatuza.

## registrarVenta
O(log(A) + log(I) + log(P) + log(cant)). Registra una venta en la instancia de puesto indicado por parametro. Aplica automaticamente el maximo descuento posible para esa cantidad.

## hackear
O(log(A) + log(I)), O(log(A) + log(I) + log(P)) en caso de que el puesto correspondiente deje de ser hackeable para esa persona e item luego de la operacion. Dada una persona y un item, se elimina del puesto de menor ID en el que la persona haya consumido sin promocion el consumo de una unidad de dicho item.

## personas
O(1). Devuelve el conjunto de personas registradas en el sistema.

## puestos
O(1). Devuelve el diccionario de pares (idpuesto,puesto), es decir, la id del puesto junto a su instancia correspondiente.

## idMenorStock
O(P*log(I)). Dado un item I, devuelve la id del puesto con menor stock, y en caso de empate, el puesto de menor ID.

## gastoTotal
O(log(A)). Dada una persona, devuelve el gasto total que realizo en el festival.

## personaMayorGasto
O(1). Devuelve el identificador de la persona que realizo el mayor gasto en el festival.

## stockEnPuesto
O(log(P) + log(I)). Devuelve el stock de determinado item en determinado puesto.

## descuentoEnPuesto
O(log(P) + log(I) + log(cant)). Devuelve el descuento correspondiente al item dada una cantidad.

## gastoEnPuesto
O(log(P) + log(A)). Devuelve el gasto en un puesto de determinada persona.

## idPuestos
O(1). Devuelve el conjunto de ids de puestos.

## Autores:
- [@fbigiolli](https://github.com/fbigiolli/sistemaVentas)
- [@lucaveron](https://github.com/lucaveron)
- [@winga35](https://github.com/winga35)
- [@juaninaki](https://github.com/juaninaki)
