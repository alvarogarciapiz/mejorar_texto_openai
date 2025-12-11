# Mejorar Texto en cualquier applicación con LLM

Este proyecto está diseñado para facilitar la corrección automática de texto usando un modelo de lenguaje (LLM) en cualquier aplicación que uses. 


Con este script, no necesitarás copiar y pegar manualmente el texto en ChatGPT. Solo necesitas configurar el script en Raycast y podrás disfrutar de correcciones inmediatas usando el atajo del teclado.

También puedes configurarlo para hacer oneshot del modelo en cualquier lugar, no solamente corrige texto, le puedes pasar cualquier instrucción y te responderá.

**Ahora soporta modelos locales con Ollama**, permitiéndote usar modelos como Gemma, Llama, Mistral y otros sin necesidad de conexión a internet ni costos de API.

![Ejemplo Email](Images/Ejemplo_Email.gif)


## Requisitos

Antes de comenzar, asegúrate de tener los siguientes elementos:

- **Python 3**: Necesario para ejecutar el script. [Página oficial de Python](https://www.python.org/downloads/).
- Instala requests ´pip install requests´ o ´pip3 install requests´ en la terminal
- **Raycast**: Una herramienta de productividad para MAC.[ sitio web](https://www.raycast.com/).
- **Opción 1 - Clave API de OpenAI**: Llave de acceso para ejecutar el LLM. [API KEY](https://platform.openai.com/account/api-keys).
- **Opción 2 - Ollama**: Para usar modelos locales. [Ollama](https://ollama.ai/).
  

## Instalación

Sigue los pasos a continuación para configurar el entorno y habilitar la ejecución del script:

1. **Instala Raycast**: 
   - Raycast es una herramienta que mejora tu productividad en el Mac. [sitio web](https://www.raycast.com/).

2. **Importa el Script a Raycast**:
   - Descarga el script proporcionado en este repositorio.
   - Una vez que Raycast esté instalado, abre la aplicación.
   - Ve a la sección de scripts y añade un directorio con el script que has descargado.
   
3. **Configura el Modelo**:
   
   **Opción A - Usar OpenAI (por defecto)**:
   - Obtén tu clave de API de OpenAI desde su plataforma.
   - Dentro del script que has copiado, reemplaza el marcador de posición correspondiente con tu clave de API de OpenAI.
   - Asegúrate de que `USE_LOCAL_MODEL = False` en el script.
   
   **Opción B - Usar Modelo Local con Ollama**:
   - Instala Ollama desde [ollama.ai](https://ollama.ai/).
   - Descarga el modelo que desees usar, por ejemplo: `ollama pull gemma3:4b`
   - En el script, cambia `USE_LOCAL_MODEL = True`
   - Actualiza `LOCAL_MODEL` con el nombre de tu modelo (ej: "gemma2:2b", "llama2", "mistral", etc.)
   - Asegúrate de que Ollama esté corriendo (se inicia automáticamente en macOS)

4. **Asignación de Atajo de Teclado**:
   - En Raycast, establece un atajo de teclado que te permita ejecutar el script fácilmente. Esto te permitirá corregir texto con solo presionar unas teclas combinadas, sin interrumpir tu flujo de trabajo.

## Uso

Una vez configurado, puedes usar el script en cualquier aplicación que permita la selección de texto. Simplemente selecciona el texto que deseas corregir y usa el atajo de teclado que configuraste en Raycast. El script copiará el texto, lo corregirá usando el API de OpenAI o tu modelo local de Ollama y luego pegará el texto corregido en su lugar.

El modelo que estoy usando es GPT-4 mini, este es el mejor para corregir y hacer textos de manera barata, aunque si fuera solo para corregir textos se podría usar perfectamente Gemini Flash 8B ya que el precio es la mitad de barato.

Igual podrías cambiar el script para usar Claude Haiku o Sonnet 3.5, o cualquier modelo de lenguaje que quisieras. Esto te da mucha flexibilidad para hacer lo que quieras; incluso podrías llamar a la API de asistentes de OPENAI para llamar a tu propio GPT con un atajo del teclado.

## Modelos Locales con Ollama

El script ahora soporta el uso de modelos locales a través de Ollama, lo que ofrece varias ventajas:

- **Sin costos de API**: No necesitas pagar por cada solicitud
- **Privacidad**: Tus textos no se envían a servidores externos
- **Sin necesidad de conexión a internet**: Funciona completamente offline
- **Velocidad**: Dependiendo de tu hardware, puede ser más rápido

Para cambiar entre modelos, simplemente actualiza la constante `LOCAL_MODEL` en el script y reinicia Raycast.

## Conclusión

Este script automatiza un proceso que de otro modo requeriría múltiples pasos manuales, en definitiva, ahorrándote tiempo y esfuerzo. Ahora puedes disfrutar de correcciones ortográficas y gramaticales fluidas y sin complicaciones con solo un atajo de teclado.

Esto es lo que debería de estar pasando con Apple Intelligence con modelos de lenguaje ejecutados en local. Esta implementación ahora usa Ollama para ejecutar modelos localmente, ofreciendo privacidad total, sin costos y funcionamiento offline. Ya no es solo una opción viable, ¡es una realidad implementada!

Probablemente implementen pronto Apple Intelligence, que hará lo mismo.

## Autor

- **Alejandro Tinto**  
  Puedes ver más sobre mi en [LinkedIn](https://www.linkedin.com/in/alejandro-tinto/) [Youtube](https://www.youtube.com/@alet1nto)
