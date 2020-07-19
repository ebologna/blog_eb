---
title: "COVID-19, restricciones y evolución económica: exploración a partir de datos globales"
author: | 
  | Eduardo Bologna
  | **Especialización en Producción y Análisis de Información para Políticas Públicas**
  | Centro de Estudios Avanzados - Facultad de Ciencias Sociales
  | Universidad Nacional de Córdoba
date: "18 julio, 2020"
output:
  beamer_presentation:
    theme: "Berlin"
    colortheme: "beaver"
    fonttheme: "serif"
    fig_caption: false
    keep_md: true
bibliography: library.bib
TOC: TRUE
header_includes:
  usepackage(longtable)
---





# Pregunta  

## ¿Qué relación hay entre el impacto de la pandemia, las medidas remediales tomadas por cada país y las proyecciones de evolución económica?  

# No puede darse una respuesta definitiva pero, a escala de país, puede verse la relación entre:  
-	La cantidad de muertes ocurridas que pueden atribuirse al COVID-19  
-	Las medidas tomadas por cada país  
-	La evolución proyectada del PBI  


# Origen de los datos  
-	Los dos primeros provienen del proyecto *Our World in Data* [@owidcoronavirus] en https://ourworldindata.org/    


\includegraphics[width=300px]{owid_1} 


# Que ofrece, en GitHub,  


\includegraphics[width=300px]{owid_2} 



# Acceso libre a una base con 34 variables, provenientes de distintas fuentes, de las que aquí usamos



\includegraphics[width=300px]{tabla_variables_2} 


# El Fondo Monetario Internacional [@imf]  ofrece en  

- https://www.imf.org/~/media/Files/Publications/WEO/2020/Update/June/English/data/WEOJun2020update.ashx?la=en  

La actualización a junio 2020 de las estimaciones de la evolución del PBI para 30 países

# Una vez reunidas esas dos fuentes de datos, se pueden observar relaciones entre los niveles de mortalidad por COVID-19 y características de cada país  
- La información ha sido procesada con RStudio [@Team2015]  
- Usando los paquetes: readxl [@readxl], ggplot2 [@ggplot2], ggthemes [@ggthemes] y ggrepel [@ggrepel]  
- Las operaciones que conducen a estos resultados están disponibles en https://github.com/ebologna/pbi_muertes/blob/master/restricciones_muertes_pbi.Rmd  

# Datos actualizados al 2020-07-16  

# Los países con poblaciones más envejecidas han sido más afectados  ($r=$ 0.46, $p=$ 0.0248)  

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-5-1.pdf) 


# Que coinciden cercanamente con los que tienen niveles de mortalidad general más bajos ($r=$ 0.41, $p=$ 0.0485)  

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-6-1.pdf) 

# La infraestructura hospitalaria, hace leve diferencia en la mortalidad atribuida a COVID-19 ($r=$ -0.2, $p=$ 0.3612)   

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-7-1.pdf) 


# Pero es más intensa la asociación con el grado de restricción adoptado  ($r=$ -0.28, $p=$ 0.1873)  

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-8-1.pdf) 


# Los países más afectados tienen peores pronósticos de evolución del PBI ($r=$ -0.73, $p=$ \ensuremath{10^{-4}})  
![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-9-1.pdf) 

# La intensidad de las medidas de restricción se asocia levemente con las expectativas económicas  ($r=$ 0.19, $p=$ 0.3678)  

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-10-1.pdf) 


# Esta relación puede vincularse al número de muertes por millón de habitantes (en el tamaño de los puntos)  

![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-11-1.pdf) 

# O bien al número absoluto de muertes atribuidas al COVID-16  
![](restricciones_muertes_pbi_files/figure-beamer/unnamed-chunk-12-1.pdf) 



# En breve  
- La composición por edades de las poblaciones se vincula con las consecuencias de la pandemia: los países con mayor proporción de adultos mayores han tenido la mayor cantidad de muertes.  
- Las acciones estatales de tipo estructural, como la disponibilidad de camas de hospital, o coyuntural, como las medidas que limitan la circulación, muestran asociación negativa con el volumen de defunciones, pero no significativa con los datos con que se cuenta.  

# En breve  
- Aunque generalizada, la previsión negativa para la evolución del PBI es claramente más pesimista para los países que cuentan mayor proporción de muertes.  
- Las proyecciones sobre caída del PBI son generalizadas, son más acentuadas en los paises con más muertes y no se correlacionan significativamente con las medidas restrictivas.   

# Referencias  {.allowframebreaks}  
