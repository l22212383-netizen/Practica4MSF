[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=l22212383-netizen/Practica4MSF)
# Práctica 4: Regeneración de glóbulos rojos

## Información del estudiante

Iván De Jesús Fonseca Díaz \[22212383]; l22212383@tectijuana.edu.mx

Modelado de Sistemas Fisiológicos

Ingeniería Biomédica

## Docente

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura

El modelizado de sistemas fisiológicos es una herramienta importante en Ingeniería Biomédica, permite comprender el funcionamiento del cuerpo humano, así como diseñar y evaluar terapias y dispositivos médicos; se define como el proceso de formular modelos matemáticos o computacionales que representan el comportamiento y la interacción de los sistemas biológicos y fisiológicos. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional; lo anterior al proporcionar al estudiante bases sólidas para modelizar sistemas y diseñar controladores para la solución de problemas en las áreas de atención médica y del sector industrial médico. La construcción de analogías entre circuitos eléctricos y sistemas fisiológicos para la formulación de modelos matemáticos y el diseño de controladores mediante la experimentación in silico brindan herramientas de gran aplicación en el quehacer profesional del Ingeniero Biomédico.

La asignatura de Modelado de Sistemas Fisiológicos forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Utiliza las propiedades de los circuitos RLC para describir la dinámica de sistemas fisiológicos, obtener modelos matemáticos y aplicar el control clásico, esto con el objetivo de integrar los principios de la Ingeniería de Control, la Electrónica Analógica y las Ciencias de la Computación con la Anatomía y Fisiología del cuerpo humano para proporcionar descripciones cuantitativas y cualitativas de sistemas fisiológicos complejos con el objetivo de modelizar, analizar, controlar, ilustrar y predecir su dinámica tanto en el corto como en el largo plazo.

## Objetivos

1. Resolver el sistema de EDOs mediante el método de Euler (diferencias finitas).
2. Graficar el sistema de EDOs en MATLAB.
3. Considerar el caso de transfusión sanguínea del individuo.



## Descripción detallada del sistema

El modelo matemático de tres EDOs de primer orden es un modelo mecanicista de compartimento para la eritropoyesis después de la pérdida de sangre en personas sanas, fenómeno que se
puede modelizar como un proceso dináico no lineal. donde x1(t) representa el compartimento de células precursoras eritroides altamente proliferantes con respecto a la eritropoyetina, x2(t)
describe el compartimento no proliferante de células precursoras eritroides con respecto a la eritropoyetina, y x3(t) el compartimento para los eritrocitos maduros y reticulocitos sanguíneos.

Con respecto a los parámetros, X0 refleja la cantidad absoluta de células que se destinan al linaje eritroide y que maduran en el primer compartimento de cÈlulas precursoras eritroides. Las tasas de
transición y las tasas de mortalidad entre los compartimentos están dadas por k1, k2 y alpha, estas tasas son independientes de la hormona eritropoyetina. La compensación de la pérdida de sangre se describe
mediante un término de retroalimentación de los eritrocitos a las células en proliferación basado en la pérdida fraccional de eritrocitos. Con base en lo anterior, se introducen los parámetros
y beta, que se utilizan para la descripción de las características individuales de la eritropoyesis. Se asume que cada individuo tiene un recuento medio de eritrocitos indicado por el parámetro Base.

##Condiciones iniciales
x1(0) = 
   59.5225,   61.1342,   56.0637,   61.0104,   61.7191,   56.0965,   57.7169,   60.9007,   60.7727,   61.9296
x2(0) = 
   44.3897,   45.5916,   41.8102,   45.4993,   46.0278,   41.8346,   43.0431,   45.4174,   45.3220,   46.1848
x3(0) = 
  892.8375,  917.0125,  840.9550,  915.1558,  925.7863,  841.4469,  865.7529,  913.5099,  911.5911,  928.9445

##Parámetros de beta y gamma
gamma = [0.769,0.388,0.510,0.590,0.262,0.324,0.356,0.089,0.243,0.057]
beta = [1.650,0.867,1.617,2.615,1.518,2.676,0.891,2.557,0.925,0.089]

Palabras clave: Regeneración de glóbulos rojos, Sistema de EDOs, parámetros de estimación, Simulaciones numéricas.


## Lista de archivos incluidos en el repositorio

1. Cuaderno computacional de MATLAB \[.mlx].
2. Imagen de la simulación sin transfución \[.pdf].
3. Imagen de la simulación con transfución \[.pdf].

## Referencias

\[1] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

\[2] Tetschke, M., Lilienthal, P., Pottgiesser, T., Fischer, T., Schalk, E., & Sager, S. (2018). Mathematical modeling of RBC count dynamics after blood loss. Processes, 6(9), 157. https://doi.org/10.3390/pr6090157
