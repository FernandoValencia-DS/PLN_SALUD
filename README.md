# PLN_SALUD
# 🩺 Extracción de Información Clínica en Historias de Cáncer

Este repositorio contiene dos talleres prácticos enfocados en el desarrollo de herramientas de Procesamiento de Lenguaje Natural (NLP) aplicadas a historias clínicas de pacientes oncológicos. Se utilizan modelos de tipo Transformer (basados en RoBERTa) y técnicas de Fine-Tuning para tareas de Reconocimiento de Entidades Nombradas (NER), detección de negación e incertidumbre.

---

## 🧪 Taller 1: Cáncer de pulmón - Fine-tuning y validación

Se realiza el ajuste fino (`fine-tuning`) del modelo `xlm-roberta-base` sobre un corpus anotado de historias clínicas de pacientes con cáncer de pulmón. Posteriormente, se valida el modelo resultante evaluando 10 oraciones clínicas para analizar su capacidad de extracción de entidades relevantes (como diagnósticos, tratamientos, biomarcadores, etc.).

---

## 🧪 Taller 2: Cáncer de mama - Extracción + análisis de contexto

Este taller se enfoca en historias clínicas de cáncer de mama. Se integran dos modelos preentrenados:

1. **Modelo NER**: [`anvorja/breast-cancer-biomedical-ner-sp-1`](https://huggingface.co/anvorja/breast-cancer-biomedical-ner-sp-1)
   - Extrae entidades clínicas específicas (tipo de cáncer, tratamiento, biomarcadores, etc.)

2. **Modelo de negación/incertidumbre**: [`JuanSolarte99/bert-base-uncased-finetuned-ner-negation_detection_NUBES`](https://huggingface.co/JuanSolarte99/bert-base-uncased-finetuned-ner-negation_detection_NUBES)
   - Clasifica cada entidad como **Afirmativa**, **Negada** o **Sospechosa**.

🔄 Finalmente, se construye una base de datos estructurada en formato CSV con las columnas:
- `patient_id`, `sentence`, `NER`, `NER_label`, `Estado`

---

## 📚 Créditos

Desarrollado como parte de los talleres de Analítica en Salud en Salud por los estudiantes: 

- **Fernando Valencia 2401899-7727**
- **Alejandro Orozco 2402036-7727**
- **Carlos Botero 2400879-7727**
- **Brandon Rivas 2400430-7727**

