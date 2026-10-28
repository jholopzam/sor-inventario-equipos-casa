
# b0-p03-casa-inventario-equipos

- **Alumno:** Jhoseen Lopez Zambrano
- **Bloque:** B0 — Fase 0.8
- **Fase / ejercicio:** B0.P03 · Casa · Inventario de equipos
- **Fecha de inicio:** 23/10/2026
- **Fecha de entrega:** 26/10/2026

---

## 🎯 Qué se pedía

Crear un inventario de equipos desde cero en una nueva bóveda y repositorio local independientes, guardando la evolución en tres versiones con Git y conectándolas a un remoto en GitHub. Además, consultar de forma segura una versión anterior del historial sin alterar la rama principal y documentar todo el proceso en la bitácora mediante un cuarto commit.

## ⌨️ Comandos y pasos importantes

- `git init` — Inicializa el repositorio de Git exclusivamente dentro de la carpeta `01_Proyecto`.
- `git branch -M main` — Cambia y fija el nombre de la rama principal como `main`.
- `git remote add origin ...` — Conecta el repositorio local con el remoto en GitHub mediante SSH.
- `git add <archivo>` — Prepara y selecciona los archivos específicos que se incluirán en el siguiente commit.
- `git status` — Muestra el estado actual del árbol de trabajo y los archivos modificados o preparados.
- `git diff` — Compara los cambios realizados en el disco con respecto al índice.
- `git commit -m "mensaje"` — Guarda una nueva versión local del proyecto con un mensaje descriptivo.
- `git push` — Sube los commits locales al repositorio remoto en GitHub.
- `git switch --detach <código>` — Permite situarse temporalmente en un commit antiguo para consultar su estado sin modificar las ramas.
- `git switch main` — Regresa a la rama principal de trabajo.

## 🛠️ Qué he hecho

1. He preparado una ubicación local independiente fuera de OneDrive y del árbol SOR para crear la bóveda `Boveda_Inventario_Casa` junto con su estructura de carpetas inicial (`00_Grabaciones`, `01_Proyecto`, etc.).
2. He creado el `.gitignore` para excluir archivos innecesarios y de vídeo, además del `README.md` inicial y el fichero `inventario/equipos.csv` con dos equipos de prueba (`EQ01` y `EQ02`).
3. He inicializado Git en `01_Proyecto`, configurado la rama `main` y vinculado el repositorio remoto vacío de GitHub (`sor-inventario-equipos-casa`).
4. He realizado el primer commit y el primer `push` con el inventario inicial (`H5`).
5. He modificado el CSV en el paso `H6` cambiando la ubicación de `EQ01` a `Aula-3` y el estado de `EQ02` a `mantenimiento`, guardando la segunda versión y subiéndola a GitHub.
6. He llevado a cabo la ampliación (`H7`), añadiendo la carpeta de mantenimiento con la ficha de `EQ02`, el archivo de criterios de estado, la imagen de ejemplo y el equipo `EQ03`, además de incorporar los clips de vídeo locales de prueba que fueron ignorados por `.gitignore`. He preparado cada archivo de forma individual y he subido la tercera versión.
7. He consultado el primer commit utilizando `git switch --detach` para verificar el estado inicial del CSV y he regresado de forma segura a `main`.
8. He completado esta bitácora y la he subido mediante un cuarto commit documental de cierre (`H8`).

## 🚩 Qué me ha fallado y cómo lo he resuelto

- **Fallo:** Al principio intenté colocar el archivo `README.md` dentro de la carpeta `inventario`, lo que provocó que los enlaces de navegación de Obsidian no se renderizaran de manera correcta.
- **Solución:** Moví el archivo `README.md` a la raíz de `01_Proyecto` tal y como indicaba la estructura de la práctica y separé los enlaces en líneas independientes.

## 🤔 Respuestas a las preguntas

1. **¿Por qué el repositorio está en 01_Proyecto y no en la raíz de la bóveda?**
   Porque la configuración de Obsidian y las grabaciones de OBS deben permanecer separadas y fuera de la gestión de control de versiones de Git, aislando estrictamente el código del proyecto.
2. **¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?**
   Cambié la ubicación de `EQ01` de `Aula-1` a `Aula-3` y el estado de `EQ02` de `disponible` a `mantenimiento`. En el `git diff` se visualizan con un signo menos (`-`) para las líneas retiradas y un signo más (`+`) para las incorporadas.
3. **¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?**
   Editar modifica únicamente el contenido guardado en el disco local, mientras que `git add` toma esa modificación y la añade al área de preparación (*staging area*), señalando que está lista para ser incluida en el próximo commit.
4. **¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?**
   Porque la ficha nueva es un archivo sin seguimiento (*untracked*), por lo que no forma parte de las diferencias del fichero `equipos.csv`.
5. **¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?**
   Preparé individualmente `inventario/mantenimiento/EQ02.md`, `inventario/criterios-estados.md`, `inventario/imagenes/equipo.png`, `inventario/equipos.csv` y `README.md`. El comando `git diff --cached` mostró un resumen con los archivos nuevos añadidos y las modificaciones de texto y binarias listas para el commit.
6. **¿Cómo demostraste que los clips existen y están ignorados sin subirlos?**
   Mediante el comando `git check-ignore -v` aplicado a los archivos de vídeo, el cual identifica la regla del `.gitignore` que los excluye, comprobando al mismo tiempo en el gestor de archivos que seguían presentes en el disco local.
7. **¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?**
   Al viajar al primer commit, `EQ01` volvió a figurar en `Aula-1`, `EQ02` pasó a estar `disponible` y el equipo `EQ03` desapareció temporalmente ya que no formaba parte de esa versión inicial.
8. **¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?**
   Necesita historial para conservar la trazabilidad de cada cambio y entrega ante modificaciones o incidencias. Sus limitaciones residen en que carece de control de concurrencia en tiempo real, validación estricta de datos y gestión de permisos multiusuario simultáneos.
9. **¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?**
   La comprobación se realizó mediante `git status`, `git log --oneline` y la revisión directa del repositorio en GitHub. Su cierre ocurre después del vídeo porque la bitácora recopila y documenta todo el proceso completo (incluidas las marcas temporales de la grabación).

## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/Zg_5QqyofEg
- **Playlist:** https://youtube.com/playlist?list=PLOgCQzjt_2m0&si=QhKn_KofTayHZARr
- **Repositorio:** https://github.com/jholopzam/sor-inventario-equipos-casa

## 💭 Dudas / a repasar

- Ninguna duda relevante; el flujo completo de trabajo por fases, comandos y saltos de versiones ha quedado comprendido de forma clara.