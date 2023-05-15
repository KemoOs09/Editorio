<h1>Proyecto: Aplicación que permita cargar un archivo de tipo .json, Editarlo y eliminarlo </h1>
<h1>Alumno: Osorio Garcia Hugo Diego ISC 4B 62249 </h1>

<h2>Se crea el JFrame con los elementos </h2>



Se van a incluir algunas nuevas características en la aplicación, como un área de texto en la que se mostrará el
contenido del archivo seleccionado y también se podrá editar el archivo directamente allí. Además, se agregará un 
botón "Archivo" para buscar y seleccionar el archivo deseado y otro botón "Guardar" para guardar los cambios 
realizados en el archivo.

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/51d28f63480f11de72cc09a330fd3e2f5052f5be/Captura.PNG)

<h2>Dar funcionalidad al botón archivo al hacer clic.</h2>

Se implementa un JFileChooser que se activa al hacer clic en el botón correspondiente. Se utiliza un "filtro" con FileNameExtensionFilter para permitir la selección de archivos específicos, según la opción elegida en un JComboBox que permite seleccionar entre archivos de texto plano o archivos JSON. Después de seleccionar un archivo y hacer clic en "Abrir", si se selecciona "Cancelar", la aplicación no realizará ninguna acción. En caso contrario, la ruta del archivo se mostrará en un campo de texto y se insertará caracter por caracter en un String usando un bucle while, para luego ser mostrado en el TextArea correspondiente. Todo esto se encuentra dentro de un bloque try-catch para manejar errores de ejecución.

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/51d28f63480f11de72cc09a330fd3e2f5052f5be/Captura2.PNG)

<h2>Dar funcionalidad al botón guardar al hacer clic.</h2>

Primero se agregó un condicional if para comprobar si el campo de texto que muestra la ruta del archivo está vacío, lo que indica que no se ha importado ningún archivo. En tal caso, cuando se presiona el botón "Guardar", se mostrará un cuadro de diálogo para informar al usuario que debe importar un archivo primero.

Si se ha importado un archivo previamente y se han realizado cambios en el contenido del TextArea, se creará un objeto File y se utilizará un PrintWriter para escribir en él el contenido actualizado del TextArea utilizando el método print(). Finalmente, se cierra el PrintWriter para evitar cambios no deseados con close().

Todo esto se encuentra dentro de un bloque try-catch para capturar cualquier excepción de tipo FileNotFoundException y mostrarla en la consola, junto con una descripción adecuada del error.

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/51d28f63480f11de72cc09a330fd3e2f5052f5be/Captura3.PNG)

<h2>Dar funcionalidad al botón eliminar al hacer clic.</h2>

Aquí se ha agregado un bloque de código que elimina el archivo importado actualmente utilizando el método delete() de la clase File. También se utiliza una declaración condicional if para verificar si se pudo eliminar correctamente el archivo. Si la eliminación no fue exitosa, ya sea porque no se importó ningún archivo o por otro problema, se muestra un mensaje para informar al usuario.

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/51d28f63480f11de72cc09a330fd3e2f5052f5be/Captura4.PNG)

<h2>Funcionalidad del programa.</h2>

1.Al dar clic en el botón Archivo, se busca un archivo json y se da a open:

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/a73f0b1d89d7578862a92900299b7bcaa3391462/Captura5.PNG)

2.Se modifican texto en el txtArea y se guarda.

![](https://github.com/KemoOs09/Reporte-Imagenes/blob/ec36aeae4c28f9b0671b8ea1c09448f5fcc9236f/Captura6.PNG)

3.Se elimina el archivo.
