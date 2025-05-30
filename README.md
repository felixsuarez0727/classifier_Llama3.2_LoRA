# Llama_rfu_LoRa - Modelo de regresión de Péptidos

## Introducción

Este repositorio contiene el notebook `Llama_rfu_QLoRa.ipynb` para la regresión de péptidos utilizando el modelo Llama3-2_1b de Meta, implementado mediante LoRA (Low-Rank Adaptation) para optimización de recursos.

## Requisitos Previos

1. **Cuenta en Hugging Face**

   - Crear cuenta en [Hugging Face](https://huggingface.co/)
   - Generar un token de acceso con permisos de **escritura** (Settings > Tokens)
   - Aceptar las políticas de uso del modelo Llama3 en Hugging Face (https://huggingface.co/meta-llama/Llama-3.2-1B)

2. **Dependencias**

   ```bash
   !pip install -q --upgrade transformers peft trl datasets accelerate bitsandbytes scikit-learn
   ```

3. **Configuración de Token**
   Ejecutar el siguiente código en el notebook para iniciar sesión:
   ```python
   from huggingface_hub import notebook_login
   notebook_login()
   ```
   Esto abrirá una ventana emergente donde deberás ingresar tu token

## Uso

1. Clonar el repositorio
2. Ejecutar el notebook

## Resultados del Test

- **RMSE (Root Mean Squared Error):** 0.5556
- **MAE (Mean Absolute Error):** 0.4254
- **R² Score:** 0.2482

## Consideraciones Técnicas

- Implementación de LoRA para fine-tuning eficiente
- Uso de técnicas de quantización para reducir consumo de memoria
- Adaptación del modelo Llama3-2_1b para tareas de regresión de secuencias peptídicas
