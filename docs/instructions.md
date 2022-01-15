<h1 align="center">Análisis de imágenes usando el Biofilm Analyzer Software</h1>

<h2>Información sobre el experimento</h2>
<p align="justify">Usted analizará los experimentos de formación y adherencia de biopelículas de la cepa <i>Pseudomona aeruginosa</i> realizados por el <a href="https://investigacion.cayetano.edu.pe/catalogo/biotecnologia/lmi" target="_blank" rel="noreferrer noopener">Laboratorio de Moléculas Individuales</a> en el año 2019. Esta experiencia consistió en el crecimiento de biopelícula durante diferentes tiempos de incubación. Los cultivos se realizaron en una placa de 96 pocillos. Luego, las biopelículas fueron teñidas usando el reactivo cristal violeta. La distribución de controles negativos y experimentos fue la siguiente:</p>

- La columna 1 es el control negativo (medio de cultivo sin bacterias).
- De la columna 2 hasta la 8 tenemos los pocillos con medio de cultivo y bacteria a diferentes tiempos de incubación (4 a 28 horas). Las cuatro primeras filas (A,B,C y D) son réplicas. 
- Sólo se utilizaron 32 pocillos en total.

<p align="center"> <img width="450" src="multiwell-plate.jpg" alt="multiwell-plate"> </p>

<p align="justify"> Al finalizar, se tomaron fotografías de los pocillos con un microscopio digital 1000X CoolingTech, una lámpara LED de luz blanca y un filtro de acrílico blanco de 3mm. Estos son unos ejemplos de control negativo (A) y crecimiento de biopelícula (B).</p>

<p align="center"> <img width="450" src="pics-examples.jpg" alt="pics-example"> </p>

<h2>Instrucciones para el análisis de imágenes</h2>
<p align="justify">Su objetivo es obtener la cantidad de biopelícula adherida en cada uno de los 32 pocillos utilizando el Biofilm Analyzer Software (BAS). Para cumplir con este objetivo, debe seguir la siguiente lista de actividades:</p>

### PASO 0: Instalación y ejecución del BAS
- Descargar el software desde [aquí](). La carpeta comprimida también contiene las imágenes que analizará en los siguientes pasos.
- Descomprimir la carpeta, acceder a ella, y dar doble clic en el archivo BAS.exe

### PASO 1: Importación de imágenes al BAS

En la seccion **Choose Work Space** podrá ubicar e importar las imágenes para el análisis:
- Dar clic en el boton gris con puntos suspensivos.
- Buscar en ruta específica la carpeta con las imágenes de los controles negativos y biopelículas. 
- Seleccionar en ruta específica la carpeta con imágenes y dar clic en **Seleccionar carpeta**. Las imágenes se cargarán automáticamente.
- Seleccionar la imagen de referencia (control negativo) en el recuadro superior y la imagen con biopelícula en el recuadro inferior.
- Utilizar las flechas al pie de los recuadros para ir hacia delante o atrás, hasta encontrar la imagen de interés.

> **IMPORTANTE:** Para la cuantificación de la imágenes de biopelícula de cada fila, debe utilizar el control negativo que le corresponde. Por ejemplo: Si analiza las imágenes de la Fila A, debe utilizar como imagen de referencia la imagen A1 y comparar con la imagen A2, A3,..., A8. Para la Fila B, la imagen de referencia es B1, y así para cada fila.

<p align="center"> <img width="600" src="step1-BAS.jpg" alt="step1-BAS"> </p>

### PASO 2: Recorte de la región de interés de la imagen

<p align="justify">Ir a la sección Manual Segmentation, dar clic en “Segment Biofilm Well” y aparecerá un recuadro con indicaciones sobre el proceso de segmentación. La primera imagen que se muestra es la imagen de referencia. Se da clic en un extremo de la imagen, se mantiene presionado el botón izquierdo del ratón y se arrastra el puntero para seleccionar el área de interés para la segmentación. En este caso, el área de interés es el fondo del pocillo. Presionar Enter para finalizar el proceso de segmentación.</p>

<p align="center"> <img width="600" src="step2-BAS.jpg" alt="step1-BAS"> </p>

<p align="justify">Luego de segmentar el fondo del pocillo de referencia, debe segmentar el fondo del pocillo con biopelícula siguiendo los mismos pasos. Si no está conforme con la selección del área de interés, tiene dos formas de revertir la segmentación. La primera opción es no presionar Enter hasta que considere que la selección es adecuada. Puede repetir el proceso de selección varias veces dando clic en cualquier extremo de la imagen hasta obtener el área apropiada. Para finalizar, presionará Enter. La segunda opción es dando clic de nuevo en “Segment Biofilm Well” para realizar de nuevo el proceso de segmentación.</p>

### PASO 3: Selección de filtros
<p align="justify">Ir a la sección Select Color Scale para seleccionar el filtro que se utilizará para la cuantificación de biopelícula. En esta sección puede elegir entre la Escala de Grises o el Canal Verde, los filtros tienen un desempeño similar. La selección del filtro dependerá del tipo de imagen a analizar. Luego de seleccionar el filtro, dar clic en “Confirm Color Scale”para ir a la siguiente sección.</p>

### PASO 4: Cuantificación
<p align="justify">Ir a la sección Select Threshold y dar clic en “Begin Threshold” para la selección del umbral que permitirá la cuantificación. Se cargará un recuadro que muestra el Histograma de Frecuencia de Píxeles de la imagen de referencia. Los valores de píxel varían desde 0 hasta 250 (eje X). Los píxeles más oscuros serán de menor valor o se ubican más hacia la izquierda de la gráfica; mientras que, los píxeles más claros serán de mayor valor o se ubican más hacia la derecha. Para este ejemplo, se seleccionó en el paso anterior el Canal Verde. En el siguiente histograma, se puede observar que hay una gran concentración de píxeles hacia el lado derecho de la gráfica. Esta distribución se debe a que la imagen de referencia o control negativo tiene en su mayoría píxeles claros lo que representa la ausencia de biopelícula teñida.</p>

<p align="justify">Para realizar la cuantificación, usted debe definir un umbral que permitirá al software identificar qué píxeles representan biopelícula. Luego de seleccionar el umbral, BAS designa a los píxeles de la derecha como segmentos de fondo sin biopelícula, y a los píxeles de la izquierda como segmentos de biopelícula. Usualmente el valor del umbral es menor o mayor que 180. Para finalizar, dar clic en “Defined Threshold”.</p> 

### PASO 5: Exportación de resultados
<p align="justify">Ir a la sección Obtención de área y dar clic en “Show results” para visualizar la identificación de biopelícula presente en el fondo del pocillo y el porcentaje de píxeles que representan la materia orgánica. En el ejemplo presentado, BAS ha calculado que casi el 100% de los píxeles representaría a la biopelícula. Si se observa la imagen original, efectivamente, todo el fondo del pocillo está teñido, lo que significa que la biopelícula cubrió toda el área de interés. Para exportar los resultados, primero se debe guardar los datos dando clic en “Add Result” y luego “Export Excel”. Cada vez que analice una imagen, debe agregar el resultado al archivo si desea exportar todos los resultados en un sólo archivo.</p>

<p align="justify">BAS generará un archivo CSV en la carpeta donde se encuentra el archivo ejecutable del software. Los datos que se generan corresponden a Estadística Descriptiva de la distribución de píxeles de la imagen de interés y la distribución de los píxeles que representan biopelícula.</p>


