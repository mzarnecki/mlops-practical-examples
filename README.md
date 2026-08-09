# MLOps Practical Examples

Hands-on notebooks for a practical  MLOps scenarios: versioning datasets and models, tracking experiments, exposing models as APIs, serving TensorFlow models in production, comparing REST and gRPC, observing LLM applications, serving local LLMs, monitoring GPU usage, and deploying smaller models to edge devices or browsers.

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
| 01 | [01_dvc_model_versioning_demo_en.ipynb](notebooks/en/01_dvc_model_versioning_demo_en.ipynb) | DVC as Git-like versioning for datasets and model artifacts. |
| 02 | [02_MNIST_image_digit_classification_with_mlflow_en.ipynb](notebooks/en/02_MNIST_image_digit_classification_with_mlflow_en.ipynb) | MNIST image classification in PyTorch with MLflow experiment tracking. |
| 03 | [03_fastapi_flask_model_api_en.ipynb](notebooks/en/03_fastapi_flask_model_api_en.ipynb) | Exposing a trained ML model through FastAPI and Flask. |
| 04 | [04_tensorflow_serving_rest_grpc_en.ipynb](notebooks/en/04_tensorflow_serving_rest_grpc_en.ipynb) | TensorFlow Serving, model versioning, REST and gRPC inference. |
| 05 | [05_LLM_evaluation_criteria_tracking_with_langsmith_en.ipynb](notebooks/en/05_LLM_evaluation_criteria_tracking_with_langsmith_en.ipynb) | Criteria-based LLM evaluation and experiment tracking with LangSmith. |
| 06 | [06_ollama_llm_api_en.ipynb](notebooks/en/06_ollama_llm_api_en.ipynb) | Local LLM serving with Ollama. |
| 07 | [07_edge_gpu_netron_tflite_tfjs_en.ipynb](notebooks/en/07_edge_gpu_netron_tflite_tfjs_en.ipynb) | Netron, GPU monitoring with `nvidia-smi`, TensorFlow Lite/LiteRT and TensorFlow.js. |

Each notebook is available in two language versions:

- English: `notebooks/en/*_en.ipynb`
- Polish: `notebooks/pl/*_pl.ipynb`

## Articles related to this repository on medium 

[MLOps Begins Where the Notebook Ends — MLOps in Practice Part 1](https://medium.com/@brightcode/mlops-begins-where-the-notebook-ends-mlops-in-practice-part-1-e8699a74ab3e?postPublishedType=repub)   
[From Tracked Experiments to a Production Model API - MLOps in Practice Part 2](https://medium.com/@brightcode/from-tracked-experiments-to-a-production-model-api-mlops-in-practice-part-2-250e422cd3bf)   
[Safe Model Rollouts, Responsible Production ML and LLMOps— MLOps in Practice Part 3](https://medium.com/@brightcode/877fb93989e0?sharedUserId=brightcode)   


## Suggested lecture flow

1. Use DVC to explain why code versioning is not enough for ML projects.
2. Continue with MLflow to show why experiment tracking matters.
3. Expose a simple model with FastAPI or Flask.
4. Move to TensorFlow Serving to show production-oriented model serving, model versioning, REST and gRPC inference.
5. Introduce criteria-based LLM evaluation and experiment tracking with LangSmith.
6. Serve a local LLM with Ollama.
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

Praktyczne notebooki z przykładami MLOps: wersjonowanie danych i modeli, śledzenie eksperymentów, wystawianie modeli jako API, produkcyjne serwowanie modeli TensorFlow, porównanie REST i gRPC, obserwowalność aplikacji LLM, lokalne serwowanie LLM, monitoring GPU oraz wdrażanie mniejszych modeli na urządzeniach edge i w przeglądarce.

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
| 01 | [01_dvc_model_versioning_demo_pl.ipynb](notebooks/pl/01_dvc_model_versioning_demo_pl.ipynb) | DVC jako wersjonowanie danych i artefaktów modelu w stylu Git. |
| 02 | [02_MNIST_image_digit_classification_with_mlflow_pl.ipynb](notebooks/pl/02_MNIST_image_digit_classification_with_mlflow_pl.ipynb) | Klasyfikacja cyfr MNIST w PyTorch ze śledzeniem eksperymentów w MLflow. |
| 03 | [03_fastapi_flask_model_api_pl.ipynb](notebooks/pl/03_fastapi_flask_model_api_pl.ipynb) | Udostępnienie wytrenowanego modelu ML przez FastAPI i Flask. |
| 04 | [04_tensorflow_serving_rest_grpc_pl.ipynb](notebooks/pl/04_tensorflow_serving_rest_grpc_pl.ipynb) | TensorFlow Serving, wersjonowanie modeli, inferencja przez REST i gRPC. |
| 05 | [05_LLM_evaluation_criteria_tracking_with_langsmith_pl.ipynb](notebooks/pl/05_LLM_evaluation_criteria_tracking_with_langsmith_pl.ipynb) | Ewaluacja LLM według kryteriów i śledzenie eksperymentów w LangSmith. |
| 06 | [06_ollama_llm_api_pl.ipynb](notebooks/pl/06_ollama_llm_api_pl.ipynb) | Lokalne serwowanie LLM przez Ollama. |
| 07 | [07_edge_gpu_netron_tflite_tfjs_pl.ipynb](notebooks/pl/07_edge_gpu_netron_tflite_tfjs_pl.ipynb) | Netron, monitoring GPU przez `nvidia-smi`, TensorFlow Lite/LiteRT i TensorFlow.js. |

Każdy notebook jest dostępny w dwóch wersjach językowych:

- angielska: `notebooks/en/*_en.ipynb`
- polska: `notebooks/pl/*_pl.ipynb`

## Sugerowany przebieg wykładu

1. Użyć DVC do wyjaśnienia, dlaczego samo wersjonowanie kodu nie wystarcza w projektach ML.
2. Przejść do MLflow, żeby pokazać, dlaczego śledzenie eksperymentów jest ważne.
3. Wystawić prosty model przez FastAPI lub Flask.
4. Przejść do TensorFlow Serving, żeby pokazać produkcyjne serwowanie modeli, wersjonowanie, REST i gRPC.
5. Wprowadzić ewaluację LLM według kryteriów i śledzenie eksperymentów w LangSmith.
6. Uruchomić lokalny model LLM przez Ollama.
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
