# Agente-IA-BimBam-Buy
Creación de agente de inteligencia artificial que asiste al público objetivo, es decir, personas usuarios con distintas consultas en lo referido a:
*Guía de tiempos y costos de envío
*Política de reembolsos
*Programa de afiliados
*Manual de garantía 
*Preguntas frequentes- FAQs

## Descripción general
El proyecto implementa una arquitectura **RAG (Retrieval-Augmented Generation)** que permite que el modelo genere respuestas utilizando información proveniente de documentos internos de modo que sus respuestas sean más precisas, actualizadas y alineadas con la información oficial de la empresa.

# Arquitectura de la solución
El flujo de funcionamiento del agente es el siguiente:

```
                Documentos PDF
                      │
                      ▼
          Carga y procesamiento
                      │
                      ▼
        División en fragmentos (Chunks)
                      │
                      ▼
 Generación de Embeddings (Google Gemini)
                      │
                      ▼
       Base Vectorial (ChromaDB)
                      │
                      ▼
          Retriever (Búsqueda semántica)
                      │
                      ▼
               Prompt Template
                      │
                      ▼
        Modelo Gemini (Google AI)
                      │
                      ▼
      Respuesta generada al usuario
```

### Componentes principales

- **Carga de documentos**
  - Lectura de archivos PDF mediante LangChain.

- **Preprocesamiento**
  - División de los documentos en fragmentos para mejorar la recuperación de información.

- **Embeddings**
  - Conversión de los textos en representaciones vectoriales utilizando Google Generative AI Embeddings.

- **Base vectorial**
  - Almacenamiento de embeddings mediante ChromaDB.

- **Retriever**
  - Recuperación de los fragmentos más relevantes para responder cada consulta.

- **LLM**
  - Google Gemini genera la respuesta utilizando el contexto recuperado.

---

# Tecnologías y herramientas utilizadas

- Python 3
- Jupyter Notebook
- LangChain
- Google Gemini
- Google Generative AI Embeddings
- ChromaDB
- PyPDF
- dotenv
- Google Colab
- GitHub

---

# Instalación y ejecución

## 1. Clonar el repositorio

```
git clone https://github.com/mafloan/Agente-IA-BimBam-Buy.git
```

```Agente-IA-BimBamBuy2026
```
## 2. Instalar las dependencias

```
pip install langchain
pip install langchain-google-genai
pip install chromadb
pip install pypdf
pip install python-dotenv
```

## 3. Configurar la API Key

Crear un archivo `.env`

```
GOOGLE_API_KEY=TU_API_KEY
```

## 4. Ejecutar el notebook
```
Abrir: Agente_IA_BimBamBuy2026.ipynb
Aclaración: cree varios archivos pero el que funciona es Agente IA BimBamBuy2026
```
---

#Ejemplos de preguntas al Agente de IA de BimBam Buy:
Chat ready! Ask questions below:
Q: Exclusiones de la garantia
Ask about BimBam Buy policies...
RESPONSE:
------------------------------------------------------------
De acuerdo con las políticas de BimBam Buy, la garantía no cubre lo siguiente:

*   Daño por golpes o caídas.
*   Humedad, agua, calor excesivo o fuego.
*   Manipulación por terceros no autorizados.
*   Reparaciones externas.
*   Accesorios consumibles desgastados por uso natural.
*   Instalación incorrecta.
*   Incompatibilidad de uso fuera de especificación.
*   Desgaste normal.
*   Alteración de seriales.
*   Sellos manipulados.
*   Uso de accesorios no recomendados que provoquen daño.
*   Fallas originadas por mantenimiento inadecuado.
*   Daños estéticos que no afecten el funcionamiento (salvo que la normativa local disponga otra cosa).

Asimismo, se identifican como señales de no cobertura:
*   Golpes evidentes.
*   Uso fuera de instrucciones.
*   Accesorios incompatibles.
*   Modificaciones físicas.

Chat ready! Ask questions below:
Q: Postular al programa de afiliados
Ask about BimBam Buy policies...
RESPONSE:
------------------------------------------------------------
De acuerdo con las políticas de BimBam Buy, pueden postular al programa de afiliados:

* Creadores de contenido
* Sitios de cupones
* Medios digitales
* Comunidades de compras
* Educadores o reseñadores de productos
* Socios de contenido con audiencia en LATAM

El tiempo para la aprobación de los postulantes es variable.
------------------------------------------------------------

Sources:
  • Programa de afiliados.pdf
*   Exposición a líquidos o temperaturas extremas.
------------------------------------------------------------

  • Manual de Garantia.pdf
  • Politica de reembolsos.pdf
