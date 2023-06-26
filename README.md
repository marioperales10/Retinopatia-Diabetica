# Retinopatia-Diabetica

ATRIBUTOS (COLUMNAS):

  1) El resultado binario de la evaluación de la calidad. 0 = mala calidad 1 = calidad suficiente.
  2) El resultado binario de la preselección, donde 1 indica anomalía retiniana grave y 0 su ausencia.
  3-8) Los resultados de la detección de MA. Cada valor de característica representa el número de MA encontrados en los niveles de confianza alfa = 0,5, . . . , 1, respectivamente.
  9-16) contienen la misma información que 2-7) para exudados. Sin embargo,
ya que los exudados están representados por un conjunto de puntos en lugar del número de
píxeles que construyen las lesiones, estas características se normalizan dividiendo el
número de lesiones con el diámetro del ROI para compensar diferentes imágenes
tamaños
  17) La distancia euclidiana del centro de
la mácula y el centro del disco óptico para proporcionar información importante
en cuanto a la condición del paciente. Esta característica
también se normaliza con el diámetro de la ROI.
  18) El diámetro del disco óptico.
  19) El resultado binario de la clasificación basada en AM/FM.
  20) Etiqueta de clase. 1 = contiene signos de DR (Etiqueta acumulativa para las clases Messidor 1, 2, 3), 0 = sin signos de DR.


RESUMEN SOBRE EL CONJUNTO DE DATOS:

La retinopatía diabética (RD) es una consecuencia de la diabetes mellitus que se manifiesta en la retina. Esta enfermedad es una de las causas más frecuentes de discapacidad visual en los países desarrollados y es la primera causa de nuevos casos de ceguera en la población en edad laboral. En 2011, 366 millones de personas fueron diagnosticadas con diabetes y otras 280 millones estaban en riesgo de desarrollarla. En cualquier momento, aproximadamente el 40% de los pacientes diabéticos padecen RD, de los cuales aproximadamente el 5% se enfrenta a la forma de esta enfermedad que amenaza la vista. En total, casi 75 personas se quedan ciegas todos los días como consecuencia de la RD a pesar de que hay tratamiento disponible.
El cribado automático asistido por ordenador de la RD es un campo muy investigado. La motivación para crear sistemas de cribado de DR automáticos fiables es reducir el esfuerzo manual del cribado masivo, lo que también plantea un problema financiero. Si bien varios estudios se centran en el reconocimiento de pacientes con RD y consideran la especificidad de la detección como una cuestión de eficiencia, mostramos cómo tanto la sensibilidad como la especificidad se pueden mantener en un nivel alto mediante la combinación de características novedosas de detección y un proceso de toma de decisiones. Especialmente, nuestros resultados están muy cerca de cumplir con las recomendaciones de la Asociación Británica de Diabéticos (BDA) (80% de sensibilidad y 95% de especificidad).
La base de un sistema de cribado automático es el análisis de imágenes de fondo de ojo en color. La clave para el reconocimiento temprano de la RD es la detección confiable de microaneurismas (MA) en la retina, que sirve como una parte esencial para la mayoría de los sistemas automáticos de detección de RD. El papel de las lesiones brillantes para la clasificación de DR también se ha investigado con resultados positivos  y negativos . Además de las lesiones, la evaluación de la calidad de la imagen  también se considera para excluir las imágenes no clasificables. Como nueva dirección, en Agurto et al.  También se presenta un algoritmo de reconocimiento DR a nivel de imagen.
El marco propuesto amplía los componentes de última generación de un sistema automático de detección de DR al agregar la detección previa  y la distancia del centro de la mácula (MC) y el centro del disco óptico (ODC) como componentes novedosos. También usamos la evaluación de la calidad de la imagen como una función para la clasificación en lugar de una herramienta para excluir imágenes. La comparación de los componentes utilizados en algunos sistemas automáticos de detección de DR publicados recientemente se puede encontrar en la Tabla 1.
Con respecto a la toma de decisiones, los sistemas automáticos de detección de DR siguen parcialmente los protocolos clínicos (p. ej., los MA indican la presencia de DR)  o utilizan un clasificador de aprendizaje automático . Una forma común de mejorar la confiabilidad en aplicaciones basadas en aprendizaje automático es utilizar enfoques basados en conjuntos . Para el apoyo a las decisiones médicas, los métodos de conjunto se han aplicado con éxito en varios campos. En West et al. los autores han investigado la aplicabilidad de conjuntos para la clasificación de datos de cáncer de mama. La predicción de la respuesta a determinada terapia se mejora mediante el uso de un conjunto clasificador  En Eom et al. los autores utilizaron un conjunto de cuatro clasificadores para la predicción de enfermedades cardiovasculares. También se proporcionan métodos de conjunto.


Los microneurismas y los exudados son dos características distintas que pueden estar presentes en la retina y son relevantes en el contexto de la retinopatía diabética.

Los microneurismas son pequeñas dilataciones de los vasos sanguíneos de la retina. Se forman como resultado de la debilidad en las paredes de los vasos sanguíneos debido a la diabetes. Los microneurismas pueden aparecer como pequeñas protuberancias redondeadas en los vasos sanguíneos y son uno de los primeros signos de daño vascular en la retina.

Por otro lado, los exudados son acumulaciones de líquido, proteínas y lípidos que se filtran de los vasos sanguíneos dañados. En el contexto de la retinopatía diabética, los exudados pueden aparecer como manchas blancas o amarillentas en la retina. Los exudados son un signo de un mayor grado de daño vascular y pueden indicar la presencia de edema macular, una complicación grave de la retinopatía diabética.

En resumen, los microneurismas son dilataciones de los vasos sanguíneos, mientras que los exudados son acumulaciones de líquido y proteínas. Ambos son signos de daño vascular en la retina asociado con la retinopatía diabética, pero representan diferentes manifestaciones y grados de gravedad de la enfermedad.

Sin embargo, como los exudados están representados por un conjunto de puntos en lugar del número de píxeles que construyen las lesiones, estas características se normalizan dividiendo el número de lesiones por el diámetro de la ROI para compensar los diferentes tamaños de imagen.

Dado que las anomalías pueden dificultar la detección de ciertos puntos de referencia anatómicos en una imagen, v17 representa la distancia euclidiana del centro de la mácula y el centro del disco óptico para proporcionar información importante sobre el estado del paciente.

v18 es el resultado de la clasificación basada en AM/FM, que es un escalar no negativo que indica la confianza de la detección de DR. Cuanto mayor sea v18, mayor será la probabilidad de que DR esté presente. Como se puede observar en nuestro conjunto de datos, es un atributo binario.
