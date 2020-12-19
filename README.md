# ...::: Analisis de Datos | MasterPath :::...

Este es el analisis que se hizo a los datos para extraer información de valor y que ayude a la toma de decisiones.

## Page 💻
[master-app.herokuapp.com](https://masterpath-app.herokuapp.com/)
[Dashboard MasterPath](https://datastudio.google.com/reporting/442fd58e-7ef9-4aee-951f-8a09fc3d2c24)

## Stack 🛠️
- [Google Data Studio](https://datastudio.google.com/) - Herramienta gratuita que permite convertir datos en informes y paneles claros, totalmente personalizables y fáciles de consultar y compartir.
- [SQL](https://developer.mozilla.org/es/docs/Glossary/SQL) - Lenguaje de programación diseñado para actualizar, obtener, y calcular información en bases de datos relacionales.

## Autor ✒️
- **Alberto Ortiz** - _Analista de Datos_ - [CarGDev](https://github.com/CarGDev)

## Analizando los Datos
***Grafico 1***

Este grafico circular muestra al top 10 de estudiantes con mayor actividad en repositorios de GitHub. Esto permite que el coach pueda identificar rapidamente a los alumnos mas activos realizando retos.

``` select u.id, u.username, count(w.id) as works_total from works w, users u where u.id = w."userId" group by u.id, u.username order by id ```

![Alumnos con mayor actividad de repositorios]()


## Base de Datos 💾
[Modelo Relacional](https://github.com/HPM-MASSIMO-MasterPath/Backend/blob/main/BD%20Relacional%20Master%20Path.png)

## Licencia :bookmark_tabs:
Proyecto bajo la licencia MIT.
