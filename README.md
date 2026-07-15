# Agente_AluraChallenge
# Alura Agente - Asistente de Políticas Internas (NUTRIGENETICS)

## Descripción del Proyecto
Este proyecto consiste en la creación de un agente de Inteligencia Artificial capaz de interactuar con documentos internos de una empresa (en este caso, las Políticas de Cancelación, Devolución y Reembolso de NUTRIGENETICS, S.A. DE C.V.). El objetivo principal es optimizar el tiempo de los colaboradores, permitiéndoles realizar consultas en lenguaje natural y obtener respuestas directas sin necesidad de abrir ni leer manualmente los archivos.

---

## Arquitectura del Sistema
El sistema fue diseñado siguiendo un flujo simplificado de procesamiento y consulta de datos:

1. **Extracción y Procesamiento:** Se carga el documento corporativo (`documento_empresa.txt`) y se procesa su contenido en memoria estructurada usando Python.
2. **Orquestación del Agente:** Se utiliza **LangChain** para estructurar el prompt del sistema, inyectar el contexto del documento y gestionar la interacción con el usuario.
3. **Cerebro del Agente (LLM):** Se conecta con la API de **Cohere**, utilizando el modelo avanzado de lenguaje `command-a-03-2025` configurado con `temperature=0` para garantizar respuestas precisas, coherentes y basadas estrictamente en la documentación.

---

## Tecnologías Utilizadas
* **Lenguaje base:** Python 3.12
* **Framework del Agente:** LangChain
* **Modelo de Lenguaje (LLM):** Cohere (`command-a-03-2025`)
* **Entorno de Prototipado:** Google Colab

---

## Ejemplos de Preguntas y Respuestas
A continuación se muestran ejemplos reales de consultas que el agente resuelve con éxito:

* **Pregunta:** ¿Cuánto tiempo tengo para solicitar una devolución?
* **Respuesta del Agente:** Según el documento de referencia, el usuario tiene 7 (siete) días naturales siguientes a la fecha de entrega del producto para solicitar una devolución...

* **Pregunta:** ¿Puedo cancelar una compra si el producto ya fue enviado?
* **Respuesta del Agente:** No, en caso de que los Productos ya hayan sido enviados y se encuentren fuera de las oficinas de NUTRIGENETICS, el Usuario no podrá cancelar la compra realizada.

---

## Instrucciones para ejecutar (Local)
Para ejecutar este proyecto de forma local utilizando Google Colab, sigue estos pasos:

1. Abre un nuevo cuaderno en [Google Colab](https://colab.research.google.com/).
2. Crea una celda y ejecuta el código de procesamiento del documento de texto (`texto_politicas`).
3. Instala las dependencias necesarias ejecutando:
   ```bash
   pip install -q langchain-cohere langchain

## ☁️ Implementación en la Nube (Deploy OCI)
*⏳ Deploy pendiente: La implementación del agente en Oracle Cloud Infrastructure (OCI Compute) se encuentra en proceso. Se actualizará esta sección con el enlace público y las capturas de pantalla correspondientes en la siguiente fase.*
