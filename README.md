# Juntador-de-audios.
### Una herramienta simple que permite juntar varios archivos de audio, separados por silencios, en un solo archivo de audio.

<a href="https://colab.research.google.com/github/XxNessuxX/Juntador-de-audios./blob/main/Juntador_de_audios.ipynb" target="_parent"><img src"https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>

Este código es una herramienta útil para juntar varios archivos de audio en un solo archivo de audio, separados por silencios de duración definida por el usuario. Está escrito en Python utilizando la biblioteca PyDub para trabajar con archivos de audio.

El código comienza instalando PyDub usando pip y luego importa las bibliotecas necesarias, incluyendo os para trabajar con el sistema de archivos y AudioSegment de PyDub para trabajar con los archivos de audio.

El usuario puede definir la duración del silencio en milisegundos utilizando un control deslizante proporcionado por la interfaz de usuario. La duración recomendada del silencio se establece en 500 milisegundos, pero el usuario puede ajustarla en el rango de 300 a 500 milisegundos.

Luego, el código lee los archivos de audio de la carpeta "audios" y los agrega a una lista de segmentos de audio utilizando el método AudioSegment.from_wav de PyDub. Los archivos de audio deben estar en formato .wav para que el código los pueda leer correctamente.

A continuación, se crea un segmento de audio final que consiste en un silencio inicial de duración definida por el usuario, seguido de cada segmento de audio en la lista, separados por el mismo silencio. Esto se logra mediante un bucle que recorre cada segmento de audio en la lista y agrega ese segmento al segmento final, junto con silencios de duración definida por el usuario.

Finalmente, el segmento final se exporta como un archivo de audio .wav llamado "audios juntados.wav" y se descarga automáticamente utilizando la biblioteca files de Colab.

En resumen, este código proporciona una herramienta fácil de usar para combinar varios archivos de audio en uno solo, con la opción de agregar silencios entre ellos de duración definida por el usuario. Es una herramienta útil para aquellos que necesitan trabajar con varios archivos de audio y quieren combinarlos en un solo archivo para su conveniencia.
