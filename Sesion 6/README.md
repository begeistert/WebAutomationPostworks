<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/4/43/Cognizant_logo_2022.svg" alt="Logo">
  </a>

<h3 align="center">Web Automation Testing</h3>
<h4 align="center">Sesión 6 - Selenium Grid</h4>

## Integrantes

* Roberto Bertrand Lizárraga
* Iván Montiel Cardona
* Mungarro Echeverría Héctor
* Salmerón González Victor

## Desarollo
* Adaptar scripts de pruebas automatizados para que puedan ser ejecutados en múltiples navegadores (cross browser testing).
* Selecciona una funcionalidad de Mercadolibre para automatizar o una que ya tengas automatizada. Pro-Tip: es recomendable automatizar una nueva funcionalidad, de esta manera puedes tener un nuevo mecanismo de ejecución de pruebas en tu proyecto.
* Agrega la parametría al archivo `testng.xml` para que tome la información de los navegadores (2 como mínimo).
* Utiliza la anotación `@Parameters()` en clase de prueba para que consuma la parametría del archivo `testng.xml`
* Adapta los métodos de pruebas para que ejecuten las pruebas que dependen de los navegadores parametrizados.
* Construir nuevos scripts de pruebas automatizados donde se implemente la ejecución en máquinas remotas con `Selenium Grid`.
* Selecciona una funcionalidad de Mercadolibre para automatizar o una que ya tengas automatizada. Pro-Tip: es recomendable automatizar una nueva funcionalidad, de esta manera puedes tener un nuevo mecanismo de ejecución de pruebas en tu proyecto.
* Crea la clase de prueba donde se utilicen los objetos `DesiredCapabilites` y `RemoteWebDriver`.
* Inicia `Selenium Grid 4`.
* Ejecuta las pruebas automatizadas.


### Requerimientos
* Debe adaptar el archivo `testng.xml` con los datos de la parametría de los navegadores web (2 como mínimo).
* Hacer uso de anotación `@Parameters()` en clase de prueba invocando los campos parametrizados en el archivo testng.xml.
* Visualizar la ejecución exitosa de pruebas automatizadas en múltiples exploradores.
* Desarrollar una nueva clase de clase de prueba que donde se implementen los objetos: `DesiredCapabilites` y `RemoteWebDriver` para la ejecución automatizada de casos de prueba en máquinas remotas.
* Visualizar la ejecución exitosa de pruebas automatizadas en máquinas remotas con `selenium Grid`.


### Resultados

Aquí van los resultados


## Licencia
Distribuido bajo la licencia MIT. Consulte `LICENCE` para obtener más información.

##### Equipo 2