# Análisis PLN de Comunidades en Reddit 📝🤖

Este proyecto es una aplicación integral de Procesamiento del Lenguaje Natural (PLN) diseñada para analizar el comportamiento, sentimiento y contenido de las comunidades en Reddit. Utilizando técnicas que van desde el Machine Learning clásico hasta los Small Large Models (SLMs) más recientes, el sistema extrae, clasifica y evalúa miles de comentarios en tiempo real.

## 🚀 Características Principales

El flujo de trabajo del proyecto está dividido en 6 fases clave de procesamiento y análisis de datos:

* 1. Extracción y Limpieza de Datos (Scraping): Uso de la librería `PRAW` (Python Reddit API Wrapper) para compilar un corpus de aproximadamente 6000 comentarios provenientes de al menos 20 hilos en 6 subreddits distintos. Incluye preprocesamiento léxico avanzado para limpiar URLs, menciones y aplicar correcciones ortográficas. Los datos se estructuran y almacenan en ficheros JSON.


* 2. Clasificador Automático de Subreddits: Modelos predictivos para identificar a qué subreddit pertenece un comentario. El proyecto compara tres enfoques técnicos:


* 
*Baseline tradicional:* Bag of Words (BoW) y TF-IDF combinados con Random Forest y SVM.


* 
*Word Embeddings:* Uso de GloVe o fastText.


* 
*Transformers (Fine-Tuning):* Modelos Masked Language Model (MLM) como BERT, RoBERTa o BETO.




* 3. Similitud Semántica de Hilos: Generación de *sentence embeddings* a través de `fastText` (y modelos Sentence-Transformers) para calcular la similitud vectorial entre diferentes hilos y detectar discusiones relacionadas.


* 4. Análisis de Sentimiento y Emoción: Implementación de modelos contextuales preentrenados (HuggingFace) para extraer la polaridad (positivo, negativo, neutro) y las emociones subyacentes (ira, alegría, miedo, etc.) de los comentarios de los usuarios.


* 5. Resumen Abstractivo Automatizado: Generación de síntesis inteligentes de hilos completos usando modelos dedicados como `mT5_multilingual_XLSum` y estrategias Zero-shot Learning con SLMs como Gemma (2B) o Llama 3.2 (1B).


* 6. Detección de Contenido Sensible: Evaluación profunda de hilos del subreddit *OpinionesPolemicas* para moderación de contenido. Se exprimen las capacidades de razonamiento de los SLMs mediante técnicas avanzadas de prompting: *Zero-shot Learning* (ZSL), *Few-shot Learning* (FSL) y *Chain-of-Thought*.



## 🛠️ Tecnologías Utilizadas

* 
**Lenguaje:** Python 


* 
**Extracción de Datos:** PRAW (API de Reddit) 


* 
**Librerías Clásicas ML:** Scikit-learn (CountVectorizer, TfidfVectorizer, SVM, Random Forest) 


* 
**Deep Learning & NLP:** fastText, GloVe, HuggingFace Transformers (BETO, RoBERTa, mT5) 


* 
**Modelos SLM:** Gemma (2B), Llama 3.2 (1B) 
