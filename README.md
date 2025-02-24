# Portafolio de Análisis de Datos 📉📊📈
¡Bienvenido a mi portafolio de análisis de datos en GitHub! En este repositorio, encontrarás una colección de mis proyectos principales de análisis y ciencia de datos, así como un resumen de los KPIs, palancas y conclusiones obtenidas de cada uno.
## [Resultados del proyecto de inversión inmobiliaria en Madrid](https://github.com/Sergicas01/portfolio/blob/main/Madrid2024resultados.ipynb)
La empresa ha seleccionado la ciudad de Madrid como candidata para buscar inmuebles en los que invertir con el objetivo de obtener rentabilidad mediante alquiler turístico.

Las palancas que influyen sobre el objetivo de negocio son:
* **Precio alquiler:** cuanto más se pueda cobrar por noche mayor es la rentabilidad
* **Ocupación:** en general cuantos más días al año se pueda alquilar un inmueble mayor es su rentabilidad
* **Precio inmueble:** cuanto más barato se pueda adquirir la propiedad mayor es la rentabilidad

Los KPIs son:
* Mediremos la ocupación como el número de días anuales que el inmueble se pueda alquilar
* Mediremos el precio del alquiler como el precio por noche en euros según Airbnb
* Mediremos el precio de un inmueble como la multiplicación entre el número de metros cuadrados y el precio medio del m2 en su zona
### Conclusiones
* Se han localizado 8 barrios en los que centrar la búsqueda
* Se recomienda buscar inmuebles con un habitación que permitan alojar 3 huéspedes
* Se recomienda buscar inmuebles que estando en uno de los barrios identificados no estén necesariamente cerca de puntos de interés
* Se recomienda incrementar el número de reseñas del inmueble en alquiler, ya que favorece a un incremento de la ocupación del mismo.
* Se recomienda evaluar el desarrollo de un nuevo producto basado en el alquier para momentos concretos de alto interés deportivo, especialmente en el barrio de San Blas
## [Resultados del proyecto de detección de ineficiencias en una planta solar](https://github.com/Sergicas01/portfolio/blob/main/PLANTA%20SOLAR%20RESULTADOS.ipynb)
En este proyecto para una compañía de generación de energía solar fotovoltaica, se han detectado comportamientos anómalos en 2 de las plantas. Analizamos los datos de los sensores y medidores.

Las palancas que influyen sobre el objetivo de negocio (en este caso generar corriente AC) son:

* **Irradiación:** a mayor irradiación mayor DC generada. Pero no es monotónica, a partir de ciertos valores mayor temperatura puede mermar la capacidad de generación
* **Estado de los paneles:** deben estar limpios y con un correcto funcionamiento para generar la mayor energía DC posible
* **Eficiencia de los inverters:** siempre hay una pérdida en la transformación de DC a AC, pero debe ser la mínima posible. También deben estar en correcto estado y funcionamiento.
* **Medidores y sensores:** si se estropean y no miden bien perdemos la trazabilidad y la posibilidad de detectar fallos

Los KPIs son:
* **Irradiación:** mide la energía solar que llega
* **Temperatura ambiente y del módulo:** medida por los sensores de la planta en grados Celsius
* **Potencia DC:** medida los kw de corriente contínua
* **Potencia AC:** medida los kw de corriente alterna
### Conclusiones
* El hecho de que la generación en DC sea unas 10 veces superior en la planta 1 que en la 2, sumado al hecho de que la eficiencia en la planta 1 esté sobre el 10% nos lleva a pensar que el dato de generación de DC en la planta 1 puede estar artificialmente escalado por algún motivo. A falta de comprobación vamos a asumir que los datos son correctos.
* Aunque la temperatura ambiente es superior en la planta 2 y sus módulos se calientan más que los de la planta 1 esto no parece tener un impacto significativo
* La generación de DC de la planta 1 funciona bien, los módulos parecen llevar DC a los inverters.
* La generación de DC de la planta 2 NO funciona bien, algunos módulos llevan muy poco DC a los inverters incluso en las horas de mayor irradiación.
* La transformación de DC a AC de la planta 1 NO funciona bien, solo se transforma en torno al 10%, eso sí, de forma constante. Y esta baja eficiencia no es debida a momentos de no recepción de DC ni se concentra en inverters concretos, si no que parece más estructural.
* La transformación de DC a AC de la planta 2 funciona bien, ya que una vez eliminados los períodos de generación cero de DC el resto tienen una eficiencia superior al 97%
