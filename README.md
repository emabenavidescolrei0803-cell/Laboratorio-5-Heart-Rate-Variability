# Laboratorio 5 Heart Rate Variability

En este laboratorio se empleó el módulo de electrocardiografía AD8232. Antes de realizar la captura de la señal, se llevó a cabo una investigación preliminar sobre el funcionamiento del dispositivo y los principios de adquisición de señales ECG. Posteriormente, se registró la actividad eléctrica cardíaca de un sujeto durante un periodo de 4 minutos. La señal obtenida fue procesada mediante un filtro IIR, con el objetivo de mejorar su calidad y eliminar el ruido. Finalmente, se construyó un diagrama de Poincaré para analizar la variabilidad de la frecuencia cardíaca.

## PARTE A
En esta primera parte se realizó una investigación de los siguientes temas: actividad simpática y parasimpática, su efecto, la variabilidad y el diagrama de Poincaré como herramienta.

### Actividad simpática y parasimpática del sistema nervioso autónomo 

#### Actividad del Sistema Nervioso Simpático (SS)
La actividad simpática está dirigida a preparar al individuo para la defensa o la respuesta de alarma (conocida como fight or flight o lucha o huida) ante circunstancias de peligro real o potencial, garantizando la supervivencia.
#### Función y Efectos Generales
El sistema simpático es un regulador importante de la función cardíaca, especialmente cuando hay una mayor demanda metabólica de los tejidos periféricos, como ocurre durante el ejercicio.
Los efectos viscerales evidentes de la activación masiva del SS incluyen:
1. Cardiovascular: Aumento de la actividad cardíaca, lo que se traduce en un incremento de la frecuencia cardíaca (FC) y la contractilidad, y vasoconstricción periférica.
2. Respiratorio: Broncodilatación, para aumentar la entrada de aire a los pulmones.
3. Ocular: Dilatación pupilar (midriasis), para aumentar el campo visual.
4. Otros: Aumento de la glucemia, piloerección e intensa sudación.
5. Visceral: Inhibición de las funciones digestivas, urinarias y genitales.

#### Mecanismos de Acción y Neurotransmisión
- Localización Anatómica: El sistema simpático se denomina también división toracolumbar, ya que sus neuronas preganglionares se localizan en la columna intermedio-lateral de la médula espinal (entre los segmentos T1 y L2).
- Neurotransmisores: La mayoría de las neuronas posganglionares simpáticas liberan noradrenalina (NA) como neurotransmisor. Este es el producto final de una cascada que comienza a partir de la tirosina y dopamina. Sin embargo, en las glándulas sudoríparas y algunos vasos sanguíneos musculares, las posganglionares simpáticas liberan acetilcolina (ACh).
- Receptores: Los receptores posganglionares simpáticos son adrenérgicos ($\alpha$ y $\beta$).
- Irradiación: La actividad simpática provoca respuestas bastante generalizadas debido al alto grado de irradiación en los ganglios (una fibra preganglionar puede contactar con una media de 120 neuronas posganglionares), lo que amplifica la actividad. Además, la estimulación simpática activa la médula suprarrenal para liberar catecolaminas a la sangre, permitiendo la acción hormonal sobre todos los órganos efectores.

#### Actividad del Sistema Nervioso Parasimpático (SP)
La actividad del parasimpático se relaciona con las funciones protectoras y de conservación de la energía, promoviendo el correcto funcionamiento particular de los órganos viscerales.

#### Función y Efectos Generales
Los componentes funcionales del SP no actúan simultáneamente en condiciones normales, sino que participan en reflejos específicos para promover una función visceral concreta.
Las respuestas promovidas por la estimulación parasimpática incluyen:
1. Cardiovascular: Disminución de la frecuencia cardíaca y de la velocidad de conducción auriculoventricular.
2. Respiratorio: Broncoconstricción, para proteger los pulmones.
3. Ocular: Constricción pupilar (miosis), para proteger la retina de un exceso de iluminación.
4. Visceral: Aumento de la motilidad y secreciones digestivas (favoreciendo la digestión), actividad urinaria (micción) y actividad genital (erección).

#### Mecanismos de Acción y Neurotransmisión
- Localización Anatómica: El sistema parasimpático recibe la designación de división craneosacra. Sus neuronas preganglionares se sitúan en núcleos del tronco encefálico o en la columna lateral de la médula espinal sacra (S2 y S4). Los ganglios parasimpáticos yacen cerca o dentro de las estructuras viscerales (ganglios terminales), resultando en fibras posganglionares cortas.
- Neurotransmisores: Las neuronas posganglionares parasimpáticas liberan acetilcolina (ACh), que actúa sobre los receptores muscarínicos.
- Receptores: Los receptores en los órganos diana son muscarínicos.
- Irradiación: Los efectos parasimpáticos son más localizados que los simpáticos, ya que en sus ganglios, cada neurona preganglionar contacta con un número reducido de neuronas posganglionares.

### Efecto de la actividad simpática y parasimpática en la frecuencia cardíaca 

#### Efecto del Sistema Nervioso Simpático (SS)
La actividad simpática (SS) está dirigida a preparar al individuo para la respuesta de alarma o "lucha o huida" (fight or flight).
- Aumento de la Frecuencia Cardíaca (FC): La estimulación simpática produce un aumento de la actividad cardíaca. En el corazón, el sistema simpático excita las células nodales (células marcapaso del nodo sinusal), lo que resulta en un aumento de la frecuencia cardíaca.
- Disminución de la Variabilidad: La actividad del SNS aumenta la FC y disminuye la HRV (Variabilidad de la Frecuencia Cardíaca). Una VFC reducida, asociada a hiperactividad simpática, es un predictor de la mortalidad posterior a un infarto de miocardio (IAM) y de mala evolución en pacientes con insuficiencia cardíaca (IC).
- Neurotransmisor y Latencia: La mayoría de las neuronas posganglionares simpáticas liberan noradrenalina (N-A). Los efectos de la activación del SS se registran algunos latidos después, con una latencia de aproximadamente 5 segundos.
- Marcador en HRV: El componente de Baja Frecuencia (LF) de la VFC (0.04–0.15 Hz) se consideró inicialmente un marcador del SS, pero su interpretación es controversial, y podría representar el efecto combinado de las ramas simpática y parasimpática, modulado por el barorreflejo. Algunos estudios han concluido que el componente LF parece no correlacionar adecuadamente con la actividad simpática, sino con la actividad del barorreflejo.

#### Efecto del Sistema Nervioso Parasimpático (SP)
La actividad parasimpática (SP), a través del nervio vago, se relaciona con las funciones protectoras y de conservación de la energía.
- Disminución de la Frecuencia Cardíaca (FC): La estimulación del SP provoca una disminución de la frecuencia cardíaca y de la velocidad de conducción auriculoventricular. El parasimpático inhibe las células nodales, reduciendo la frecuencia.
- Aumento de la Variabilidad: La actividad del PNS disminuye la FC y aumenta la HRV.
- Mecanismo y Latencia:
1. El efecto cronotrópico negativo del SP se produce por la actividad de los receptores muscarínicos M2 de acetilcolina (ACh) en las células marcapaso              del nodo sinusal, lo que disminuye la frecuencia de los potenciales de acción.
2. Los efectos fisiológicos debidos a la activación o inactivación vagal se observan de manera casi inmediata, con una latencia aproximada de 0.05                  segundos. Esta velocidad se atribuye al rápido aclaramiento de la ACh mediado por la acetilcolinesterasa.
- Marcador en HRV: El Componente de Alta Frecuencia (HF) (0.15–0.4 Hz) se relaciona con la arritmia sinusal respiratoria y es considerado un marcador de la actividad de la rama parasimpática (tono vagal).

### Variabilidad de la frecuencia cardíaca (HRV) obtenida a partir de la señal electrocardiográfica (ECG)

La Variabilidad de la Frecuencia Cardíaca (VFC), o HRV por sus siglas en inglés (Heart Rate Variability), es uno de los indicadores principales del funcionamiento del Sistema Nervioso Autónomo (SNA). Su medición tradicional se realiza a partir de la señal electrocardiográfica (ECG).
La VFC es el fenómeno fisiológico de la variación que existe latido a latido en el tiempo, específicamente en la duración de los intervalos entre latidos. Este cambio constante en el intervalo latido a latido se debe a la interacción entre el sistema nervioso parasimpático (SP) y el simpático (SS), modulados por múltiples factores como centros corticales y subcorticales, así como baro y quimiorreceptores periféricos.
A continuación, se detalla cómo se obtiene y se analiza la HRV a partir de la señal ECG según las fuentes:

#### 1. Obtención de la señal ECG y la secuencia RR
La señal ECG es un registro gráfico de la actividad eléctrica generada por el miocardio durante el ciclo cardíaco.
#### Detección y Medición
La medición de la VFC se basa en el electrocardiograma (ECG), donde se detecta cada una de las ondas R y se calcula el tiempo entre las diferentes ondas R consecutivas, conocido como el intervalo RR ($RR_i$). La serie de intervalos RR es lo que constituye la HRV

- Frecuencia de Muestreo y Precisión: Para una estimación precisa del tiempo de ocurrencia de la onda R (con una precisión requerida de 1 a 2 ms), la frecuencia de muestreo del ECG debe ser de al menos 500 a 1000 Hz. Una frecuencia inferior a 500 Hz puede causar una distorsión crítica en los resultados del análisis de HRV, particularmente en la estimación del espectro.
- Detección QRS: La detección de los complejos QRS (picos R) es esencial para medir la HRV. El método Pan-Tompkins es uno de los algoritmos utilizados, caracterizado por su velocidad de cálculo y robustez, que implica un preprocesamiento (filtrado, derivación, cuadratura), integración y reglas de decisión con umbrales adaptativos para diferenciar los picos R de posibles ondas T pronunciadas o ruido.
- Re-muestreo y Artefactos: La secuencia RR obtenida no está muestreada uniformemente, por lo que es necesario re-muestrearla a una frecuencia constante (por ejemplo, 2 Hz o 4 Hz) e interpolarla (a menudo con interpolación polinómica de orden 3 o cúbica) para obtener una serie temporal uniforme adecuada para el análisis espectral.
- Eliminación de Artefactos: El preprocesamiento cuidadoso de los datos RR es crucial, ya que artefactos técnicos (detecciones erróneas) o fisiológicos (latidos ectópicos) pueden interferir. El método de Kaplan utiliza un modelo autorregresivo para identificar y corregir artefactos (impulsos o no linealidades) en la secuencia RR, efectuando la corrección mediante interpolación y conservando el número original de muestras.

#### 2. Métodos de Análisis de HRV
Una vez procesada la secuencia RR, los parámetros estadísticos para la caracterización de la VFC se valoran en dominios específicos:
#### A. Dominio Temporal
Es la descripción más básica de la variabilidad. Los parámetros se expresan en unidades de tiempo (ms) y analizan los lapsos entre complejos QRS:
- SDNN (Desviación estándar de todos los RRi normales): Refleja la variación general (tanto a corto como a largo plazo) dentro de la serie RR.
- rMSSD (Raíz cuadrada de la diferencia entre RRi normales adyacentes): Mide la variabilidad a corto plazo, latido a latido. Es igual a la desviación estándar de las sucesivas diferencias de intervalo RR (SDSD) para series estacionarias.
- pNN50 (Porcentaje de RRi adyacentes con una diferencia de duración mayor a 50 ms): Otra medida de la variabilidad a corto plazo.
- Otros parámetros: Promedio del intervalo RR ($RR_i$), desviación estándar de los promedios de los $RR_i$ (SDANN), y frecuencia cardíaca promedio (HR prom).

#### B.  Dominio Frecuencial
Estos parámetros cuantifican las fluctuaciones cíclicas del $RR_i$ mediante un análisis de la densidad espectral de potencia (PSD), descomponiendo la VFC en componentes oscilatorios.
Las bandas de frecuencia utilizadas para registros de corta duración (5 minutos) son:
##### 1. Componente de Alta Frecuencia (HF):
 - Rango de 0.15 a 0.4 Hz.
 - Mide la VFC debida a la arritmia sinusal respiratoria.
 - Su principal regulador es el sistema nervioso parasimpático (SP), por lo que se utiliza como marcador de la actividad del SP.
##### 2. Componente de Baja Frecuencia (LF): 
- Rango de 0.04 a 0.15 Hz.
- Su interpretación ha sido controversial.
- Representa un efecto combinado entre las ramas simpática y parasimpática.
- Ocurre en sincronización con las fluctuaciones fisiológicas de la presión arterial y se correlaciona directamente con el barorreflejo.
##### 3. Componente de Muy Baja Frecuencia (VLF):
- Rango de 0.003 a 0.04 Hz.
- Es un indicador de la termorregulación y la descarga simpática.
##### 4. Razón LF/HF:
Se ha utilizado para establecer el balance entre el SP y el SS. Sin embargo, su utilidad es debatida, ya que el SS y el SP no siempre actúan de manera recíproca.

#### C. Métodos Geométricos y No Lineales
Existen otros métodos utilizados para el análisis de la VFC:
- Métodos Geométricos: Se calculan a partir del histograma del intervalo RR. Incluyen el Índice Triangular HRV (HRVi), el TINN (ancho de la línea base del histograma RR), y el Índice de Estrés de Baevsky (SI).
- Métodos No Lineales: Teniendo en cuenta la complejidad de los sistemas de control, se utilizan para analizar las propiedades no lineales de la HRV. Incluyen el Gráfico de Poincaré (o plot de Lorenz), la entropía aproximada (ApEm), la entropía muestral (SapEm), y el análisis de fluctuación de tendencia (FDA). El gráfico de Poincaré transforma la fluctuación RR en puntos distribuidos en un plano bidimensional, que generalmente forman una configuración elipsoidal.

#### 3. Implicaciones y Utilidad
El análisis de la HRV se ha utilizado ampliamente en la investigación y en la clínica como un método no invasivo para determinar la actividad del SNA.
- Pronóstico y Riesgo: La disminución de la VFC se asocia con una menor adaptabilidad de la regulación cardiovascular y se relaciona con una mayor morbimortalidad. Se ha relacionado con un aumento en la mortalidad posterior a un infarto del miocardio, y con un riesgo aumentado de muerte súbita y taquiarritmias ventriculares fatales.
- Patologías: Las aplicaciones involucran una gran variedad de campos, incluyendo enfermedades cardiovasculares y sus factores de riesgo (como hipertensión, insuficiencia cardíaca), así como psicopatologías (depresión, ansiedad, estrés).
- Control del Ejercicio: La VFC es útil para monitorear el efecto del entrenamiento, la capacidad de trabajo y el rendimiento físico en atletas. A corto plazo, el ejercicio produce una disminución rápida de la VFC, relacionada con la inhibición del SP. A largo plazo, el entrenamiento físico produce un aumento de la VFC.

### Diagrama de Poincaré como herramienta de análisis de la serie R-R

El Diagrama de Poincaré (también conocido como plot de Lorenz o gráfico de recurrencia) es una herramienta de análisis no lineal que se utiliza para evaluar la Variabilidad de la Frecuencia Cardíaca (VFC) a partir de la serie de intervalos R-R (Intervalos entre complejos QRS consecutivos) obtenidos de la señal electrocardiográfica (ECG).
El análisis de la VFC, en general, se considera uno de los principales indicadores del funcionamiento del Sistema Nervioso Autónomo (SNA). 
A continuación, se detalla el uso del Diagrama de Poincaré y su relación con la VFC y el Balance Autonómico, según la información disponible:

#### 1. Construcción y Componentes del Diagrama de Poincaré
El Diagrama de Poincaré es un gráfico bidimensional que transforma la fluctuación R-R en puntos distribuidos en un plano.
- Construcción: Se crea trazando el intervalo R-R actual ($I_k$) contra el intervalo R-R inmediatamente siguiente ($I_{k+1}$).
- Configuración Visual: En sujetos sanos, la distribución de estos puntos generalmente adopta una configuración elipsoidal en el plano,. Esta configuración puede cambiar visualmente con la alteración autonómica,.
- Datos Requeridos: Para realizar esta evaluación, se ha sugerido que tan solo 100 intervalos R-R (que en la mayoría de los casos son menos de 2 minutos) son suficientes para la evaluación de la función autonómica cardíaca (FAC) a corto plazo.

##### Ejes y Significado Fisiológico
El análisis de la configuración elipsoidal permite calcular dos componentes principales que reflejan distintos aspectos de la fluctuación R-R,:
A.  Eje Transversal ($T$ o SD1): Este eje es perpendicular (vertical) a la línea de identidad ($I_k = I_{k+1}$).
- Refleja la variación latido a latido (beat-to-beat variation) en el tacograma (la serie temporal de intervalos R-R),.
- Una gran diferencia entre dos intervalos adyacentes resulta en un punto trazado lejos de la línea de identidad y un valor grande para $T$.
B. Eje Longitudinal ($L$ o SD2): Este eje es paralelo a la línea de identidad ($I_k = I_{k+1}$).
- Refleja la amplitud general de la fluctuación (overall amplitude),.
- Si la fluctuación es grande pero continua (gran amplitud, pero pequeña variación latido a latido), los puntos se distribuyen ampliamente a lo largo de la línea de identidad, resultando en un $L$ grande y un $T$ pequeño.

Ambos componentes ($T$ y $L$) se calculan generalmente como cuatro veces las desviaciones estándar de los puntos trazados a lo largo de sus respectivos ejes, lo cual ayuda a aproximar la imagen visual del plot.

#### 2. Diagrama de Poincaré y Balance Autonómico
El Diagrama de Poincaré es un método que ha demostrado ser útil para cuantificar la función autonómica. Se ha utilizado para derivar índices sensibles a la función de las ramas simpática y parasimpática del SNA:
- Índice Vagal Cardíaco (CVI): Este índice, derivado del Diagrama de Poincaré (específicamente la medida $\log_{10}(L/T)$), ha demostrado ser un índice sensible a la función vagal cardíaca (parasimpática) que no es afectado por la actividad simpática.
- Índice Simpático Cardíaco (CSI): La razón $L/T$ (LrT ratio o $SD2/SD1$) es un índice de la función simpática cardíaca que no se ve afectado por la actividad vagal (excepto en condición de reposo supino).

##### A. Interpretación Visual y Autonómica:
La forma del diagrama se relaciona directamente con la modulación autonómica:
- El área de la elipse se vuelve más grande a medida que la actividad vagal (parasimpática) se eleva.
- La configuración se vuelve más larga y estrecha a medida que la actividad simpática se eleva.

Los índices derivados del Diagrama de Poincaré (S1, S2 y S2/S1) han sido utilizados en estudios que comparan la VFC (obtenida por ECG) con la Variabilidad de la Frecuencia de Pulso (PRV, obtenida por fotopletismografía, PPG). Dicha comparación reveló que la diferencia entre estas dos medidas, aunque pequeña, produce una discrepancia significativa en los índices de Poincaré.

#### 3.  Contexto de la VFC y el Balance Autonómico
La Variabilidad de la Frecuencia Cardíaca (VFC) es el fenómeno de la variación de la duración de los intervalos entre latidos. Su existencia se debe a la interacción constante entre el Sistema Nervioso Parasimpático (SP) y el Sistema Nervioso Simpático (SS), que son los componentes eferentes del SNA.
Tradicionalmente, el análisis del equilibrio autonómico se realiza mediante el dominio frecuencial.
- Componente de Alta Frecuencia (HF): Se relaciona con la arritmia sinusal respiratoria y el comportamiento de la rama parasimpática,, y se utiliza como marcador de su actividad.
- Componente de Baja Frecuencia (LF): Representa el efecto combinado entre las ramas simpática y parasimpática, y está modulado por el barorreflejo,,.
- Razón LF/HF: Esta razón se ha utilizado para establecer el balance entre el SP y el SS, aunque su interpretación es controversial, ya que el SP y el SS no siempre actúan de manera recíproca. En contraste, el Diagrama de Poincaré ofrece una forma de medir la influencia de cada rama de forma separada a través de sus índices $T$ y $L$,.

Los métodos no lineales, incluido el Diagrama de Poincaré, complementan el análisis de dominio temporal y frecuencial, reconociendo la complejidad de los sistemas de control del corazón.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Luego de la investigación se realizo la captura de la señal con ayuda del módulo AD8232, en donde se registró durante 4 minutos. En los dos primeros minutos, la persona permaneció quieta, sin ningún movimiento, y en los dos minutos restantes leyó un texto.
La captura se realizó con el siguiente codigo:

```python
import nidaqmx                     # Librería daq. Requiere haber instalado el driver nidaqmx
from nidaqmx.constants import AcquisitionType # Para definir que adquiera datos de manera consecutiva
import matplotlib.pyplot as plt    # Librería para graficar
import numpy as np                 # Librería de funciones matemáticas

#%% Adquisición de la señal por tiempo definido

fs = 2000          # Frecuencia de muestreo en Hz. Recordar cumplir el criterio de Nyquist
duracion = 20    # Periodo por el cual desea medir en segundos
senal = []          # Vector vacío en el que se guardará la señal
dispositivo = 'Dev4/ai0' # Nombre del dispositivo/canal (se puede cambiar el nombre en NI max)

total_muestras = int(fs * duracion)

with nidaqmx.Task() as task:
    # Configuración del canal
    task.ai_channels.add_ai_voltage_chan(dispositivo)
    # Configuración del reloj de muestreo
    task.timing.cfg_samp_clk_timing(
        fs,
        sample_mode=AcquisitionType.FINITE,   # Adquisición finita
        samps_per_chan=total_muestras        # Total de muestras que quiero
    )

    # Lectura de todas las muestras de una vez
    senal = task.read(number_of_samples_per_channel=total_muestras)

t = np.arange(len(senal))/fs # Crea el vector de tiempo 
plt.plot(t,senal)
plt.axis([0,duracion,-6,6])
plt.grid()
plt.title(f"fs={fs}Hz, duración={duracion}s, muestras={len(senal)}")
plt.show()
#%%
np.savetxt(f"labo fs{fs}.txt", [t,senal])
```
Para así guardar los datos en un archivo TXT y luego graficar los datos con el siguiente codigo:

```python
import numpy as np
import matplotlib.pyplot as plt

# === CONFIGURACIÓN ===
ruta = "/content/senal_ECG_20251112_150635.txt"     # <-- cambia esta ruta
duracion_total = 240   # segundos (2 minutos)
segmento = 240          # duración de cada gráfica en segundos

# === CARGAR DATOS ===
data = np.loadtxt(ruta)
t = data[:, 0]
x = data[:, 1]

# === CORTAR A LOS PRIMEROS 2 MINUTOS ===
mask_total = t <= duracion_total
t = t[mask_total]
x = x[mask_total]

# === DIVIDIR EN SEGMENTOS DE 60 s ===
num_segmentos = int(np.ceil(duracion_total / segmento))

plt.figure(figsize=(10, 4))
for i in range(num_segmentos):
    inicio = i * segmento
    fin = (i + 1) * segmento
    mask = (t >= inicio) & (t < fin)

    plt.subplot(num_segmentos, 1, i + 1)
    plt.plot(t[mask], x[mask])
    plt.title(f"Segmento {i+1}: {inicio:.0f}s a {fin:.0f}s")
    plt.xlabel("Tiempo [s]")
    plt.ylabel("Amplitud [V]")
    plt.grid(True)

plt.tight_layout()
plt.show()
```
Obteniendo la siguiente grafica:

<img width="988" height="390" alt="image" src="https://github.com/user-attachments/assets/c5456831-57ce-47e6-a030-3435c73e3de4" />

## PARTE B 

En esta segunda parte se aplica un pre-procesaiento de esta señal, diseñando un filtro IIR de acuerdo con los parametros dde la señal, para luego obtener la ecuación teniendo en cuenta que la señal se divide en dos segamentos y por ultimo asumiendo parámetros inciales en 0,  estos calculos se evidencian en la siguiente imagen:

<img width="899" height="1028" alt="image" src="https://github.com/user-attachments/assets/22c4adf8-7377-4ecb-8ad6-4a3ef281edb4" />

![WhatsApp Image 2025-11-15 at 10 12 35 PM](https://github.com/user-attachments/assets/feb36187-00bb-4d74-9550-5326b2daf408)

![WhatsApp Image 2025-11-15 at 10 12 57 PM](https://github.com/user-attachments/assets/97a558bb-c3bf-4029-aa04-9f8cbe6b92ba)


Obteniendo el siguiente codigo para aplicar el filtro pasa banda.

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import butter, filtfilt

# === CONFIGURACIÓN ===
ruta = "/content/senal_ECG_20251112_150635.txt"     # <-- cambia esta ruta
duracion_total = 240      # segundos grabados (ejemplo)
segmento = 240            # duración de cada gráfico en segundos
fs = 2000                 # frecuencia de muestreo real

# === CARGAR DATOS (2 columnas: tiempo y señal) ===
data = np.loadtxt(ruta)
t = data[:, 0]
x = data[:, 1]

# === DISEÑO DEL FILTRO PASA BANDA ===
f_p1 = 0.5     # Hz  (borde inferior de pasabanda)
f_p2 = 40.0    # Hz  (borde superior de pasabanda)
orden = 3      # porque el prototipo fue N=3 y el BP → 2N

Wn = [f_p1 / (fs/2), f_p2 / (fs/2)]
b, a = butter(orden, Wn, btype='bandpass')

# === APLICAR FILTRO ===
x_f = filtfilt(b, a, x)

# === GRAFICAR POR SEGMENTOS ===
muestras_segmento = int(segmento * fs)

plt.figure(figsize=(14,6))

plt.subplot(2,1,1)
plt.plot(t, x, color='gray')
plt.title("Señal ECG original")
plt.xlabel("Tiempo [s]")
plt.ylabel("Amplitud")

plt.subplot(2,1,2)
plt.plot(t, x_f, color='blue')
plt.title("ECG filtrado 0.5–40 Hz (Butterworth orden 3)")
plt.xlabel("Tiempo [s]")
plt.ylabel("Amplitud")

plt.tight_layout()
plt.show()

# === GUARDAR SEÑAL FILTRADA ===
np.savetxt("/content/senal_filtrada.txt",
           np.column_stack((t, x_f)),
           fmt="%.8f")

print("Listo: señal filtrada guardada como 'senal_filtrada.txt'")
```
Teniendo así la siguiente grafica:

<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/de24db21-9453-4baf-88cd-e79ba89d7f28" />

luego se identifican los picos R en los dos segmentos, calculando los  intervalos e los segmentos R-R y obteniendo una nueva señal, esto se evidencia con el siguiente codigo:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import find_peaks


ruta = "/content/senal_filtrada.txt"

data = np.loadtxt(ruta)
t = data[:, 0]
x_f = data[:, 1]

fs = 2000
duracion_segmento = 120
N_segmento = int(duracion_segmento * fs)


seg1 = x_f[0:N_segmento]
t1 = t[0:N_segmento]

seg2 = x_f[N_segmento:2*N_segmento]
t2 = t[N_segmento:2*N_segmento]


dist_min = int(0.25 * fs)
umbral1 = 0.3 * np.max(seg1)
umbral2 = 0.3 * np.max(seg2)


picos1, _ = find_peaks(seg1, distance=dist_min, height=umbral1)
picos2, _ = find_peaks(seg2, distance=dist_min, height=umbral2)


tR1 = t1[picos1]
tR2 = t2[picos2]

RR1 = np.diff(tR1)
RR2 = np.diff(tR2)


np.savetxt("/content/RR_segmento1.txt", RR1, fmt="%.6f")
np.savetxt("/content/RR_segmento2.txt", RR2, fmt="%.6f")

print("RR_segmento1.txt y RR_segmento2.txt generados correctamente.")


plt.figure(figsize=(16,8))

# Segmento 1 con R detectados
plt.subplot(3,1,2)
plt.plot(t1, seg1)
plt.plot(tR1, seg1[picos1], "ro")
plt.title("Segmento 1 (0–120 s) con picos R")
plt.xlabel("Tiempo [s]")

# Segmento 2 con R detectados
plt.subplot(3,1,3)
plt.plot(t2, seg2)
plt.plot(tR2, seg2[picos2], "ro")
plt.title("Segmento 2 (120–240 s) con picos R")
plt.xlabel("Tiempo [s]")

plt.tight_layout()
plt.show()
```

Obteniendo las siguientes señales:

<img width="1590" height="543" alt="image" src="https://github.com/user-attachments/assets/436553d5-b713-4d84-bcfc-9f3acb333d11" />

Para fianlizar esta parte se realizo una comparacion de los parámetros básicos de la HRV en el dominio del tiempo , con la medida de los intervalos R-R y su desviación estandar entre ambos segmentos, esto se realizo con el siguiente codigo:

```python
import numpy as np

mean_RR1 = np.mean(RR1)
sdnn1 = np.std(RR1, ddof=1)
mean_RR2 = np.mean(RR2)
sdnn2 = np.std(RR2, ddof=1)

print("==========================================")
print("   PARÁMETROS HRV — DOMINIO DEL TIEMPO")
print("==========================================")

print("\n► Segmento 1 (0–120 s):")
print(f" Media RR   : {mean_RR1:.4f} s")
print(f" SDNN       : {sdnn1:.4f} s")

print("\n► Segmento 2 (120–240 s):")
print(f" Media RR   : {mean_RR2:.4f} s")
print(f" SDNN       : {sdnn2:.4f} s")

if mean_RR2 < mean_RR1:
    print("\n↓ La media RR es menor en el segmento 2 → mayor frecuencia cardíaca")
else:
    print("\n↑ La media RR es mayor en el segmento 2 → menor frecuencia cardíaca")

if sdnn2 < sdnn1:
    print("↓ La variabilidad (SDNN) es menor en el segmento 2 (menos variación).")
else:
    print("↑ La variabilidad (SDNN) es mayor en el segmento 2 (más variación).")
```

Teniendo como resultado los siguientes datos:
==========================================

   PARÁMETROS HRV — DOMINIO DEL TIEMPO


► Segmento 1 (0–120 s):
 Media RR   : 0.6541 s
 SDNN       : 0.0537 s

► Segmento 2 (120–240 s):
 Media RR   : 0.6235 s
 SDNN       : 0.1446 s

↓ La media RR es menor en el segmento 2 → mayor frecuencia cardíaca

↑ La variabilidad (SDNN) es mayor en el segmento 2 (más variación).

## PARTE C 



## BIBLIOGRAFIA 
1. "VARIABILIDAD DE LA FRECUENCIA CARDÍACA COMO INDICADOR DE LA ACTIVIDAD DEL SISTEMA NERVIOSO AUTÓNOMO: IMPLICACIONES EN EL EJERCICIO Y PATOLOGÍAS." (También referida en su versión en inglés como Detection Heart Rate Variability as an Indicator of Autonomic Nervous System Activation: Implications in Exercise and Pathologies). Este artículo fue publicado en la Revista Médica de la Universidad de Costa Rica, Volumen 11, Número 1, Artículo 5.
2. "Fisiología del sistema nervioso autónomo". Este artículo fue escrito por X. Navarro y se publicó en la Revista de Neurología (REV NEUROL 2002; 35 (6): 553-562).
3. "SISTEMA PARA EL ESTABLECIMIENTO DE LA RELACIÓN ENTRE LAS MEDIDAS PRV (VARIABILIDAD DE LA FRECUENCIA DE PULSO) Y HRV (VARIABILIDAD DE LA FRECUENCIA CARDIACA)". Este documento es un Trabajo de Grado de Cristhian Felipe Patiño Zambrano y Mateo Cortés López para optar por el título de Ingenieros Biomédicos.
4. "A new method of assessing cardiac autonomic function and its comparison with spectral analysis and coefficient of variation of R–R interval". Este artículo fue publicado en el Journal of the Autonomic Nervous System en 1997.
5. "DESARROLLO Y VALIDACIÓN DE ALGORITMOS PARA EL ESTUDIO DE LA VARIABILIDAD DE LA FRECUENCIA CARDIACA EN ADULTOS MAYORES". Este documento es una tesis de Freddy Andres Parra Orellana.
6. "Análisis de Variabilidad de la Frecuencia Cardiaca durante Estrés y Relajación empleando Señales Adquiridas con un Smartphone". Los autores de este estudio incluyen a Ruth V. Acero, Ezequiel Acero, y Bersain A. Reyes.
7. "EL SISTEMA NERVIOSO AUTÓNOMO. SIMPÁTICO Y PARASIMPÁTICO. CATECOLAMINAS. BARORRECEPTORES". Este es el Capítulo 3 del libro Insuficiencia Cardíaca Crónica por Fernando de la Serna.
