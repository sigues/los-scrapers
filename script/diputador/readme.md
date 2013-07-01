Estos scrappers los hice a finales del 2011-principios del 2012, sirven para extraer y clasificar la informaci�n de la p�gina oficial de los diputables (http://www.diputados.gob.mx/inicio.htm), incluyo el dise�o de la base de datos que est� en MySQL Workbench, pero al igual incluyo el archivo .sql con los datos de todos los diputados de la legislatura 2009-2012.
La verdad no recuerdo al 100% como funciona, pero es cuesti�n de hecharle una revisada y lo hechamos a andar, la �ltima vez que lo intent� fu� con la legislatura actual y funcion� de maravilla.

* comisiones.php saca las comisiones y las almacena en la tabla comisiones.php se nutre con 
 * //http://sitl.diputados.gob.mx/LXII_leg/listado_de_comisioneslxii.php?tct=1
 * //http://sitl.diputados.gob.mx/LXII_leg/listado_de_comisioneslxii.php?tct=2

* distritos.php saca estados, ciudades por estado, y distritos por ciudad 
 * http://www.ife.org.mx/documentos/DISTRITOS/planos_distritales_seccionales.html
 
* index.php saca los diputados por estado y distrito, 
 * se nutre de http://sitl.diputados.gob.mx/LXII_leg/listado_diputados_gpnp.php?tipot=TOTAL

* iniciativas.php un peque�o ejemplo, fu� el script inicial, compar� iniciativas de 30 diputados y 14 las ten�an repetidas, de eso deriv� la inquietud de hacer los dem�s scrappers, 
este script 

* integrantes.php saca los integrantes de cada comision y los almacena en bbdd

* iniciativasComision.php este mounstruo es el que saca todas las iniciativas, las clasifica y las almacena, recorre las comisiones que se sacaron con comisiones.php, ah� viene el link

* El proyecto original est� en: https://github.com/sigues/diputador

Ejecut� los scripts el 01-Julio-2013 para obtener lso datos de la legislatura LXII, los nuevos resultados est�n en diputappLXII.sql