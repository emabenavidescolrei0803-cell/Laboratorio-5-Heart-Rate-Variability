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
### Diagrama de Poincaré como herramienta de análisis de la serie R-R


Luego dee la investigación se realizo la captura de la señal con ayuda del módulo AD8232, en donde se registró durante 4 minutos. En los dos primeros minutos, la persona permaneció quieta, sin ningún movimiento, y en los dos minutos restantes leyó un texto.
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

## PARTE B 



## PARTE C 



## BIBLIOGRAFIA 
1. "VARIABILIDAD DE LA FRECUENCIA CARDÍACA COMO INDICADOR DE LA ACTIVIDAD DEL SISTEMA NERVIOSO AUTÓNOMO: IMPLICACIONES EN EL EJERCICIO Y PATOLOGÍAS." (También referida en su versión en inglés como Detection Heart Rate Variability as an Indicator of Autonomic Nervous System Activation: Implications in Exercise and Pathologies). Este artículo fue publicado en la Revista Médica de la Universidad de Costa Rica, Volumen 11, Número 1, Artículo 5.
2. "Fisiología del sistema nervioso autónomo". Este artículo fue escrito por X. Navarro y se publicó en la Revista de Neurología (REV NEUROL 2002; 35 (6): 553-562).
3. "SISTEMA PARA EL ESTABLECIMIENTO DE LA RELACIÓN ENTRE LAS MEDIDAS PRV (VARIABILIDAD DE LA FRECUENCIA DE PULSO) Y HRV (VARIABILIDAD DE LA FRECUENCIA CARDIACA)". Este documento es un Trabajo de Grado de Cristhian Felipe Patiño Zambrano y Mateo Cortés López para optar por el título de Ingenieros Biomédicos.
4. "A new method of assessing cardiac autonomic function and its comparison with spectral analysis and coefficient of variation of R–R interval". Este artículo fue publicado en el Journal of the Autonomic Nervous System en 1997.
5. "DESARROLLO Y VALIDACIÓN DE ALGORITMOS PARA EL ESTUDIO DE LA VARIABILIDAD DE LA FRECUENCIA CARDIACA EN ADULTOS MAYORES". Este documento es una tesis de Freddy Andres Parra Orellana.
6. "Análisis de Variabilidad de la Frecuencia Cardiaca durante Estrés y Relajación empleando Señales Adquiridas con un Smartphone". Los autores de este estudio incluyen a Ruth V. Acero, Ezequiel Acero, y Bersain A. Reyes.
7. "EL SISTEMA NERVIOSO AUTÓNOMO. SIMPÁTICO Y PARASIMPÁTICO. CATECOLAMINAS. BARORRECEPTORES". Este es el Capítulo 3 del libro Insuficiencia Cardíaca Crónica por Fernando de la Serna.
