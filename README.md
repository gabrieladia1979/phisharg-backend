# PhishARG Backend

Servicio de análisis de correos desarrollado con Python y FastAPI.

## Requisitos

- Python 3.10+
- pip

## Instalación

```bash
pip install -r requirements.txt
pip install -r requirements-hybrid.txt
python -m spacy download es_core_news_sm
```

## Ejecución local

Iniciar el servidor de desarrollo en `http://127.0.0.1:8001`:

```bash
uvicorn main:app --host 127.0.0.1 --port 8001 --reload
```

## Docker

Compilar y levantar el contenedor en el puerto `8080`:

```bash
docker build -t phisharg-backend .
docker run -p 8080:8080 phisharg-backend
```

## Variables de entorno

- `PHISHARG_TOKEN_KEY`: clave secreta para validar tokens de análisis.
- `PHISHARG_CORS_ORIGINS`: orígenes permitidos por CORS.
- `PHISHARG_HYBRID_MODEL_DIR`: ruta local al directorio del modelo híbrido.
- `PHISHARG_SLM_MODEL_PATH`: ruta local al modelo GGUF de explicación.
