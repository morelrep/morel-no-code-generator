Para recuperar en Zotero los metadatos y extractos de este archivo, por país

1. Cambia el valor del país en el forloop, ```{% if book.nacionalidad == "Venezuela" %}```
2. Corre el servidor y abre la página
3. Copia la tabla y ábrela en Libre Office
4. Haz una búsqueda de ```"country": ""``` y asegúrate de que no hay obras de esa nacionalidad que no están registradas
5. Si hay obras de esa nacionalidad sin registrar, agrégale el dato al registro correspondiente en ```_books``` y repite 4
6. Si no hay ninguna obra que agregar, exporta el archivo al proyecto ```wa-gbAPI-gatekeeping``` como ```books_morella.csv``` y ejecuta el script ```parser_to_zotero```
7. Importa a Zotero el archivo ```zotero_output_morela.rdf```
8. Abre el proyecto ```morelcoop.github.io``` y copia de la carpeta ```img``` los archivos indicados en el campo "call number" // otras opciones de automatización fueron evaluadas, pero dado que Zotero no permite importación masiva de adjuntos, lo más sano es hacerlo así, sobre todo considerando que esto es tarea de una sola vez //
