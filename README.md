Script 8 Automatización de pruebas de la aplicación web

Descripción del Proyecto Este proyecto vamos a automatizar el paso a paso para pedir un taxi y completar los items requeridos por la página web para concluir con el pedido satisfactoriamente.

Documentación y requisitos antes de realizar la prueba: Python: Requerimos usar Python para realizar las pruebas Pytest: DNecesitamos descargar pytest para ejecutar las pruebas en el proyecto Selenium WebDriver: Requerimos descargar Selenium y su controlador para realizar las pruebas correspondientes Localizadores: en este caso requerimos los siguientes localizadores (ID - CLASS_NAME - XPATH - CSS_SELECTOR) para ubicar en la pagina web mediante la inspección de html usando Google e interactuar con los elementos

Tecnologías Utilizadas Python: Usamos esta herramienta para poder efectuar las pruebas automatizadas correspondientes a la aplicación

PyCharm es un entorno de desarrollo integrado (IDE) utilizado en el lenguaje de la progrmación

Selenium es un conjunto de herramientas y bibliotecas de software utilizado principalmente para la automatización de pruebas en aplicaciones web.

Estructuración de pruebas automatizadas mediante POM. Configuración y limpieza utilizando setup_class que genera el entorno de la prueba inicial, luego configurando el WebDriver y el comando teardown_class para finalizar las pruebas y limpiar el uso del controlador.

Inivio Clonar el Repositorio de github

El primer paso es clonar el proyecto original y trabajar en local para realizar dichas pruebasm podemos utilizar el siguiente comando:

git clone git@github.com:NilCerquera/qa-project-Urban-Grocers-es.git "Para otro usuario, deberá modificar NilCerquera y dejar el usuario correspondiente"

Posterior a esto, configuramos pycharm y localizamos la carpeta donde se guaró nuestro proyecto, ahora bien, iniciamos el proyecto

Configurar Entorno de Pruebas
Inicialmente instalamos Pytest y selenium, ejecutamos los siguientes comandos:

pip install pytest pip install selenium

Ejecutar el Proyecto
Antes de ejecutar las pruebas, debemos actualizar la URL ya que pierde su ubicacion y es necesario refrescar la URL

Actualizas la url copiandolo en data, modificas la variable urban_routes_url actualizando entre '', la nueva URL

Declaras los localizadores por acción que requerimos para el entorno, en resumen sería lo siguiente para seguir el proceso de las pruebas automatizadas

Localiza el cuadro de texto "Desde"
Ingresa la dirección "desde"
Localiza el cuardo de texto " Hasta"
Ingresa la dirección "Hasta"
Localiza el botó pedir taxi
Click en el botó pedir taxi
Localiza la opción "Comfort"
Click en la opción comfort
Localiza el cuadro "Número de teléfono"
Click en el botón "Número de telefono
agrega el número de telefono
Localiza el bóton " Confirmar"
Presiona el boton "Confirmar
Localiza el botón "codigo"
Agrega el codigo enviado con la funcion otorgada en el proyecto inicial
Localiza el boton "Confirmar"
Presiona el botón " Confirmar"
Localiza el objeto "Método de pago"
Selecciona el botón "Metodo de pago"
Localiza el cuadro "Agregar tarjeta"
Presiona el botón agregar tarjeta
Localiza el cuadro "Número de tarjeta"
Ingresa el número de tarjeta
Localiza el cuadro "Codigo tarjeta"
Ingresa el número de codigo
en este caso, debes hacer un click en el boton TAB en cada cuadro para que se active el boton agregar
Localiza el boton agregar
Presiona el botó agregar
Localiza el cuadro "X"
Presiona click en la x
Localiza el slider Mantas y pañuelos
oprimes el slider para activar la opción
Localiza la opcion helado
Agregas 2 helados al pedido
Localiza pedir el botón pedir taxi
Presiona el botón pedir taxi
Espera que se acabe el temporizador para conocer los detalles del pedido
Para comprobar las pruebas automatizadas, requerimos usar assert para comprobar los resultados esten acordes con lo requerido de las pruebas.

Ejecución de pruebas
pytest main.py Asegúrate de revisar y actualizar los requisitos del proyecto.

Cordialmente

Nilton Cerquera QA engineer 2024
