<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a>
    <img src="https://upload.wikimedia.org/wikipedia/commons/4/43/Cognizant_logo_2022.svg" alt="Logo">
  </a>

<h3 align="center">Web Automation Testing</h3>
<h4 align="center">Sesión 4 - Captura de Datos</h4>

## Integrantes

* Roberto Bertrand Lizárraga
* Iván Montiel Cardona
* Mungarro Echeverría Héctor
* Salmerón González Victor

## Desarollo
Para este Postwork deberás crear 3 clases distintas según el cumplimiento de los siguientes objetivos:

* Emplear fuentes de datos externas (csv) como insumos de entrada de datos para los scripts
	* Importa la dependencia POM.xml de opencsv
	* Crea tu archivo csv con los datos de pruebas requeridos para cualquier funcionalidad de Mercadolibre. Pro-tip: puedes tener uno o más csv si te ayuda con la organización de los casos
	* Crea una clase llamada DataDrivenTestingUsingCSVInSelenium donde incluirás los casos de prueba de una funcionalidad de Mercadolibre tomando el csv como origen de datos, puedes utilizar la siguiente clase de base:
```java
package com.bedu.web_automation_course;

import java.io.FileReader;
import java.io.IOException;
import org.testng.annotations.Test;
import com.opencsv.CSVReader;
import com.opencsv.exceptions.CsvValidationException;

public class DataDrivenTestingUsingCSVInSelenium {  
    //Indicar la ubicación del archivo csv
    String CSV_PATH = "/Users/corinamora/BEDU/Web_Automation_Testing/Web-Automation-Testing-2022/test.csv";
    //Declaración de la variable de la clase CSVReader
    private CSVReader csvReader;
    //Declaración de una variable para leer los datos del csv
    String[] csvCell;

    @Test
    public void dataRead_CSV() throws IOException, CsvValidationException {
        //Creación del objeto de tipo CSVReader
        csvReader = new CSVReader(new FileReader(CSV_PATH));

        //uso de un loop para la lectura de todos los datos del csv 
        while ((csvCell = csvReader.readNext()) != null) {

          // se guardan en variables las posiciones del archivo csv
            String pais = csvCell[0];
            String capital = csvCell[1];
            System.out.println("El pais es : " + pais + " y su capital es :" + capital);

        }
    }
}
```
* Hacer uso de la anotación @DataProviders como insumos de entrada de datos para los scripts.
	* Crea una clase que contenga el método Dataprovider, con los datos de prueba, trata de que sean los mismos que colocaste en el csv, de manera que puedas construir 2 mecanismos de origen de datos en tu proyecto, puedes usar la siguiente clase como base:

```java
package com.bedu.web_automation_course;

import org.testng.annotations.DataProvider;

public class base
{
  @DataProvider (name = "nombre_dataprovider")
    public Object[][] metodoDataProvider(){
	    return new Object[][] {
	      {"Venezuela"}, 
	      {"Caracas"},
	      {"Argentina"},
	      {"Buenos Aires"},
	      {"Colombia"}, 
	      {"Bogotá"},
	      {"Ecuador"}, 
	      {"Quito"}
		};
  }
}
```

* Crea una clase de prueba, al igual que el ejemplo anterior, que contenga casos de prueba asociados a cualquier funcionalidad de Mercadolibre y que la misma haga el llamado a la clase dataprovider por medio del atributo:
```java
@Test(dataProvider = "dataprovider", dataProviderClass = data_provider.class)
```

### Requerimientos

* Construcción de datos de prueba en archivo csv.
* Desarrollo de clase con test que reciban datos del archivo csv.
* Desarrollo de clase con método DataProvider.
* Desarrollo de clase con tests que usen los datos de la clase con el DataProvider.

### Resultados

Código Fuente : [source](https://github.com/begeistert/WebAutomationPostworks/raw/main/Sesion%204/Sesion04Modulo03Complemento.zip)


## Licencia
Distribuido bajo la licencia MIT. Consulte `LICENCE` para obtener más información.

##### Equipo 2
