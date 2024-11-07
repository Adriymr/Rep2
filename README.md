# Rep2
Tarea
#Tarea →Adriana Martínez Ríos → Progamación#   

>especies <- data.frame(
+     especie = c("Ajolote", "Rana", "Serpiente", "Tortuga"),
+     habitat = c("Lago", "Río", "Bosque", "Lago"),
+     tamano = c(30, 10, 150, 50),
+     peso = c(150, 25, 1000, 500)
+ )
> 
> especies
>    especie habitat tamano peso
1   Ajolote    Lago     30  150
2      Rana     Río     10   25
3 Serpiente  Bosque    150 1000
4   Tortuga    Lago     50  500
> especiesf <- especies[especies$habitat == "Lago",]
> especiesf
  especie habitat tamano peso
1 Ajolote    Lago     30  150
4 Tortuga    Lago     50  500
> especieso <- especiesf[order(-especiesf$tamano), ]
> 
> especieso
  especie habitat tamano peso
4 Tortuga    Lago     50  500
1 Ajolote    Lago     30  150
> library(ggplot2)
> 
> data(iris)
>   ggplot(iris, aes(x = Sepal.Length, y = Sepal.Width, color = Species)) +
+     geom_point() +
+     labs(title = "Gráfico de Dispersión de Sepal Length vs Sepal Width")
+     estudiante = c("Ana", "Carlos", "Lucía", "Jorge", "Ana", "Carlos", "Lucía", "Jorge"),
+     asignatura = c("Matemáticas", "Matemáticas", "Matemáticas", "Matemáticas", "Historia", "Historia", "Historia", "Historia"),
+     calificacion = c(95, 85, 92, 88, 78, 82, 85, 90)
+ )
+ ![image](https://github.com/user-attachments/assets/d986370c-73ff-4b13-965d-aaf92a764738)

>
> calificaciones
  estudiante  asignatura calificacion
1        Ana Matemáticas           95
2     Carlos Matemáticas           85
3      Lucía Matemáticas           92
4      Jorge Matemáticas           88
5        Ana    Historia           78
6     Carlos    Historia           82
7      Lucía    Historia           85
8      Jorge    Historia           90
> promedio<- aggregate(calificacion ~ estudiante, data = calificaciones, FUN = mean)
>
> promedio
  estudiante calificacion
1        Ana         86.5
2     Carlos         83.5
3      Jorge         89.0
4      Lucía         88.5
> 
> alturas <- data.frame(
+     nombre = c("Laura", "Pedro", "Sara", "Miguel"),
+     altura_cm = c(160, 175, 150, 180)
+ )
> 
> alturas$metros <- alturas$altura_cm / 100
> 
> alturas
  nombre altura_cm metros
1  Laura       160   1.60
2  Pedro       175   1.75
3   Sara       150   1.50
4 Miguel       180   1.80
> 
> ventas <- data.frame(
+     mes = c("Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio"),
+     ventas = c(12000, 15000, 13000, 16000, 17500, 14000)
+ )
> ggplot(ventas, aes(x = mes, y = ventas)) +
+     geom_bar(stat = "identity", fill = "pink") +
+     labs(title = "Ventas por mes", x = "Mes", y = "Ventas")
+ ![image](https://github.com/user-attachments/assets/57a6ddfb-c7ac-41f2-bbaf-19e6aaac00f9)

>
> productos$ingresos <- productos$precio * productos$cantidad_vendida
> 
> productos
  producto precio cantidad_vendida ingresos
1        A     20              100     2000
2        B     35              200     7000
3        C     50              150     7500
4        D     10              250     2500
> ggplot(mtcars, aes(x = factor(cyl), y = mpg)) +
+     geom_boxplot() +
+     geom_jitter(color="pink", size=0.4, alpha=0.9) +
+     theme(
+         legend.position="none",
+         plot.title = element_text(size=11)
+     ) +
+     labs(title = "Distribución de MPG por Número de Cilindros", x = "Número de Cilindros", y = "Millas por Galón")
+ ![image](https://github.com/user-attachments/assets/e26aaedc-03e5-4e66-89d4-effe75b34051)

  
