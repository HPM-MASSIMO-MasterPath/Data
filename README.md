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
***Grafico 1 | Alumnos con mayor actividad en repositorios.***

Este grafico circular muestra al top 10 de estudiantes con mayor actividad en repositorios de GitHub. Esto permite que el coach pueda identificar rapidamente a los alumnos mas activos realizando retos.

``` select u.id, u.username, count(w.id) as works_total from works w, users u where u.id = w."userId" group by u.id, u.username order by id ```

![](https://raw.githubusercontent.com/HPM-MASSIMO-MasterPath/Data/main/Alumnos%20mayor%201.%20actividad.png)


***Grafico 2 | Estatus General de Learning Paths***

Este grafico hace una comparacion del total de alumnos comparando sus Learning Paths entre el total de alumnnos, los alumnos con LP asignada y de estos los alumnos que ya concluyeron con sui LP.

``` Query en proceso ```

![](https://raw.githubusercontent.com/HPM-MASSIMO-MasterPath/Data/main/2.%20Estatus%20de%20LP.png)


***Grafico 3 | Nivel de experiencia de skills de alumnos***

Este grafico permite saber del universo de alumnos en que tecnologias existe mayor enfoque y la cantidad de alumnos por nivel de experiencia en cada tecnologia ***

```
select su."skillId" as skill_id, s2."name" as name_skill, su.expertise as expertise, count(su.expertise) as total from 
	skills_users su , users u2, skills s2 
where 
	u2.id = su."userId" and s2.id = su."skillId"
group by 
	skill_id, name_skill, expertise
order by 
	skill_id, expertise asc 
```

![](https://raw.githubusercontent.com/HPM-MASSIMO-MasterPath/Data/main/3.%20Experiencia%20de%20Alumnos.png)

## Base de Datos 💾
[Modelo Relacional](https://github.com/HPM-MASSIMO-MasterPath/Backend/blob/main/BD%20Relacional%20Master%20Path.png)

## Licencia :bookmark_tabs:
Proyecto bajo la licencia MIT.
