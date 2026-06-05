# MLOps Practical Examples

Hands-on notebooks for a practical lecture on MLOps: versioning datasets and models, tracking experiments, exposing models as APIs, serving TensorFlow models in production, comparing REST and gRPC, observing LLM applications, serving local LLMs, monitoring GPU usage, and deploying smaller models to edge devices or browsers.

The repository is intentionally notebook-first. It is designed for lectures, workshops and screencasts where each topic can be demonstrated step by step.

## Repository structure

```text
mlops-practical-examples/
├── notebooks/
│   ├── en/   # English notebooks
│   └── pl/   # Polish notebooks
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
```

## Notebooks

| # | Notebook | Topic |
|---|---|---|
| 01 | `01_dvc_model_versioning_demo` | DVC as Git-like versioning for datasets and model artifacts. |
| 02 | `02_fastapi_flask_model_api` | Exposing a trained ML model through FastAPI and Flask. |
| 03 | `03_tensorflow_serving_rest_grpc` | TensorFlow Serving, model versioning, REST and gRPC inference. |
| 04 | `04_ollama_llm_api_langsmith_context` | Local LLM serving with Ollama and the LLMOps context of LangSmith. |
| 05 | `05_edge_gpu_netron_tflite_tfjs` | Netron, GPU monitoring with `nvidia-smi`, TensorFlow Lite/LiteRT and TensorFlow.js. |
| 06 | `06_LLM_evaluation_criteria_tracking_with_langsmith` | Criteria-based LLM evaluation and experiment tracking with LangSmith. |
| 07 | `07_MNIST_image_digit_classification_with_mlflow` | MNIST image classification in PyTorch with MLflow experiment tracking. |

Each notebook is available in two language versions:

- English: `notebooks/en/*_en.ipynb`
- Polish: `notebooks/pl/*_pl.ipynb`

## Suggested lecture flow

1. Start with MLflow to show why experiment tracking matters.
2. Use DVC to explain why code versioning is not enough for ML projects.
3. Expose a simple model with FastAPI or Flask.
4. Move to TensorFlow Serving to show production-oriented model serving and version replacement.
5. Compare REST and gRPC as inference protocols.
6. Add LLMOps with Ollama and LangSmith.
7. Finish with practical deployment concerns: GPU monitoring, Netron, TensorFlow Lite/LiteRT and TensorFlow.js.

## Installation

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Some examples require additional tools that are not installed by `pip`, for example:

- Docker for TensorFlow Serving.
- Ollama for local LLM serving.
- NVIDIA drivers and CUDA-compatible setup for real GPU monitoring.
- Git and DVC initialized in the project directory for the DVC workflow.

## Notes

The examples are educational and intentionally compact. In production systems you would usually add Docker images, CI/CD, automated tests, authentication, model registry policies, observability, rollback procedures, monitoring of data drift and model quality, and infrastructure-as-code.

## License

MIT License. See `LICENSE`.

---

# Praktyczne przykłady MLOps

Praktyczne notebooki do wykładu o MLOps: wersjonowanie danych i modeli, śledzenie eksperymentów, wystawianie modeli jako API, produkcyjne serwowanie modeli TensorFlow, porównanie REST i gRPC, obserwowalność aplikacji LLM, lokalne serwowanie LLM, monitoring GPU oraz wdrażanie mniejszych modeli na urządzeniach edge i w przeglądarce.

Repozytorium jest celowo oparte na notebookach. Nadaje się do wykładów, warsztatów i screencastów, w których każdy temat można pokazać krok po kroku.

## Struktura repozytorium

```text
mlops-practical-examples/
├── notebooks/
│   ├── en/   # notebooki po angielsku
│   └── pl/   # notebooki po polsku
├── requirements.txt
├── LICENSE
├── .gitignore
└── README.md
```

## Notebooki

| # | Notebook | Temat |
|---|---|---|
| 01 | `01_dvc_model_versioning_demo` | DVC jako wersjonowanie danych i artefaktów modelu w stylu Git. |
| 02 | `02_fastapi_flask_model_api` | Udostępnienie wytrenowanego modelu ML przez FastAPI i Flask. |
| 03 | `03_tensorflow_serving_rest_grpc` | TensorFlow Serving, wersjonowanie modeli, inferencja przez REST i gRPC. |
| 04 | `04_ollama_llm_api_langsmith_context` | Lokalne serwowanie LLM przez Ollama i kontekst LLMOps z LangSmith. |
| 05 | `05_edge_gpu_netron_tflite_tfjs` | Netron, monitoring GPU przez `nvidia-smi`, TensorFlow Lite/LiteRT i TensorFlow.js. |
| 06 | `06_LLM_evaluation_criteria_tracking_with_langsmith` | Ewaluacja LLM według kryteriów i śledzenie eksperymentów w LangSmith. |
| 07 | `07_MNIST_image_digit_classification_with_mlflow` | Klasyfikacja cyfr MNIST w PyTorch ze śledzeniem eksperymentów w MLflow. |

Każdy notebook jest dostępny w dwóch wersjach językowych:

- angielska: `notebooks/en/*_en.ipynb`
- polska: `notebooks/pl/*_pl.ipynb`

## Sugerowany przebieg wykładu

1. Zacząć od MLflow, żeby pokazać, dlaczego śledzenie eksperymentów jest ważne.
2. Użyć DVC do wyjaśnienia, dlaczego samo wersjonowanie kodu nie wystarcza w projektach ML.
3. Wystawić prosty model przez FastAPI lub Flask.
4. Przejść do TensorFlow Serving, żeby pokazać produkcyjne serwowanie modeli i podmianę wersji.
5. Porównać REST i gRPC jako protokoły inferencji.
6. Dodać LLMOps z Ollama i LangSmith.
7. Zakończyć praktycznymi aspektami deploymentu: monitoring GPU, Netron, TensorFlow Lite/LiteRT i TensorFlow.js.

## Instalacja

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Część przykładów wymaga dodatkowych narzędzi, które nie są instalowane przez `pip`, na przykład:

- Docker dla TensorFlow Serving.
- Ollama do lokalnego serwowania LLM.
- Sterowniki NVIDIA i konfiguracja zgodna z CUDA do realnego monitoringu GPU.
- Git i zainicjalizowane DVC w katalogu projektu dla workflow DVC.

## Uwagi

Przykłady są edukacyjne i celowo kompaktowe. W systemach produkcyjnych zwykle dodaje się jeszcze obrazy Docker, CI/CD, automatyczne testy, autoryzację, polityki model registry, obserwowalność, procedury rollbacku, monitoring driftu danych i jakości modelu oraz infrastructure-as-code.

## Licencja

MIT License. Szczegóły w pliku `LICENSE`.
