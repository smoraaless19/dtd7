<!-- 
Nombre: Sergio Morales 
Curso: ASIR1 
Fecha: 06/04/2025 
Ejercicio: DTD7 
-->

<!-- 
 Documento XML con DTD interna.
 Los errores estaban en la DTD interna, ya han sido corregidos.
-->

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE factura [
  <!-- 
  Una factura contiene cliente, fecha y una o más líneas.
  Cada línea tiene descripción, unidades y precio.
  -->

  <!ELEMENT factura (cliente, fecha, linea+)>
  <!ELEMENT cliente (#PCDATA)>
  <!ELEMENT fecha (#PCDATA)>
  <!ELEMENT linea (descripcion, unidades, precio)>
  <!ELEMENT descripcion (#PCDATA)>
  <!ELEMENT unidades (#PCDATA)>
  <!ELEMENT precio (#PCDATA)>
]>

<!--  Factura con varias líneas -->
<factura>
  <cliente>María López</cliente>
  <fecha>2025-04-06</fecha>

  <!-- Línea 1 -->
  <linea>
    <descripcion>Ratón inalámbrico</descripcion>
    <unidades>1</unidades>
    <precio>19.99</precio>
  </linea>

  <!--  Línea 2 -->
  <linea>
    <descripcion>USB 64GB</descripcion>
    <unidades>3</unidades>
    <precio>9.50</precio>
  </linea>
</factura>
