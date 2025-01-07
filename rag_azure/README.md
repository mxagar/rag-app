# RAG on Azure

Structure:

```
📁 rag_azure/
├── 📁 frontend/
│   ├── gui.py                        # Streamlit application code
│   ├── requirements.txt              # Python dependencies for the frontend
│   ├── 📁 static/                    # Static assets (images, CSS, etc.)
│   ├── 📁 templates/                 # Streamlit HTML templates (if needed)
│   └── 📁 tests/                     # Frontend-specific tests
├── 📁 backend/
│   ├── app.py                        # FastAPI server code
│   ├── requirements.txt              # Python dependencies for the backend
│   ├── 📁 routers/                   # FastAPI route definitions
│   ├── 📁 services/                  # Business logic (e.g., interacting with Azure services)
│   ├── 📁 models/                    # Pydantic models for request/response validation
│   └── 📁 tests/                     # Backend-specific tests
├── 📁 docker/
│   ├── Dockerfile-Frontend           # Dockerfile for Streamlit frontend
│   ├── Dockerfile-Backend            # Dockerfile for FastAPI backend
│   └── docker-compose.yaml           # Optional: Compose file for local development
├── 📁 infra/
│   ├── main.tf                       # Entry point for Terraform scripts
│   ├── variables.tf                  # Input variables for Terraform
│   ├── outputs.tf                    # Output variables for Terraform
│   ├── 📁 modules/
│   │   ├── 📁 vnet/                  # Virtual Network and Subnets
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   ├── 📁 ai_search/             # Azure AI Search
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   ├── 📁 container_backend/     # Backend container app
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   ├── 📁 container_frontend/    # Frontend container app
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   ├── 📁 storage/               # Azure Blob Storage
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   └── 📁 openai/                # Azure OpenAI service
│   │       ├── main.tf
│   │       ├── variables.tf
│   │       └── outputs.tf
├── 📁 .github/
│   ├── 📁 workflows/
│   │   ├── deploy-terraform.yml      # GitHub Actions for infrastructure deployment
│   │   ├── build-and-deploy.yml      # CI/CD for Docker images and container apps
├── 📁 scripts/
│   ├── init.sh                       # Initialization scripts (e.g., setup environment variables)
│   ├── local-run.sh                  # Script to run the app locally with Docker Compose
│   └── test.sh                       # Script for running tests
├── .env                              # Environment variables for local development
├── .gitignore                        # Ignore unnecessary files
├── README.md                         # Documentation for the project
└── LICENSE                           # License file

```