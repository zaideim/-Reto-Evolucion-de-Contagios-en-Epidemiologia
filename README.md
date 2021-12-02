# -Reto-Evolucion-de-Contagios-en-Epidemiologia
Reto - Fase 4: Contagios considerando movimiento aleatorio

En este código realizado en Python se puede observar cómo es que se comporta un sector de la población respecto a los contagios, dicha modelación se realiza por medio de ecuaciones diferenciales en el lenguaje de programación antes mencionado. Este tipo de modelación funciona para poder visualizar e incluso pronosticar cómo es que las curvas de contagios se comportan para de esta manera corregir la evolución de la enfermedad. 

Nuestra Fase 3 fue una parte fundamental de nuestra situación problema ya que fue una base para poder empezar a crear nuestra simulación. Inicialmente tuvimos que crear una ciudad con distribuciones de personas diferentes dónde ocupamos como variable D para definir el tamaño de dicha ciudad y con la variable N se definió el número de personas de la ciudad. En resumen, tuvimos que construir 4 ciudades con las diferentes especificaciones tales como: ciudad cuadrada con distribución uniforme, ciudad circular con distribución uniforme, ciudad cuadrada con distribución en cluster y ciudad circular con distribución en cluster.

Ahora se creó un ciclo para poder manejarlo con un número de iteraciones, para cada una de las iteraciones estamos creando dos vectores de tamaño N en el cual vamos a almacenar los desplazamientos de las N personas que estamos utilizando, para el desplazamiento lo que haremos es manejarlos con números aleatorios con distribuciones normales, esto lo realizamos para poder visualizar y describir cual es la distancia y la dirección en la que se están moviendo las personas, para poder así tener un mejor análisis de lo que estamos haciendo en los vectores de tamaño. 

Después, el vector de desplazamiento individual fue sumado a la posición de cada individuo. Se crearon dos estructuras de datos para almacenar la primera estructura de datos para los infectados de la iteración actual, y en otra, los datos de la iteración siguiente. 
 
Para poder determinar si una persona susceptible había sido contagiada, en cada iteración se calculó la distancia de estos a las personas infectadas y si esta distancia era menor a 0.6, el estatus de la persona cambiaría de “susceptible” a “infectado”. Además, para determinar si uno de los infectados se recuperaba de la enfermedad, se les asignó un número aleatorio entre 0 y 1, y si este era menor que la tasa de recuperación, su estado cambiaría a ser “recuperado”. 

Se decidió que se harían 365 iteraciones para considerar un año, por lo que cada iteración se fue guardando en un data frame nuevo. Finalmente todos los data frames fueron juntados para poder hacer la animación.

Para realizar una animación que pudiera mostrar de manera gráfica cómo iba evolucionando la enfermedad, cómo se iba contagiando más gente y recuperando otros más se utilizó “plotly”. De esta manera, de los data frames obtenidos anteriormente para cada iteración se graficaron y se muestran tres diferentes colores para “recuperados”, “susceptibles” e “infectados”.
