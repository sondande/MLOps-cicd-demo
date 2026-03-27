# MLOps CI/CD Demo (Student Friendly)

This repo demonstrates a complete CI/CD pipeline for ML models.

## Flow
- Train model
- Evaluate with quality gate
- Run tests
- Build Docker image

## Local Run
pip install -r requirements.txt
python src/train.py
python src/evaluate.py
uvicorn app.main:app --reload

## CI/CD
- GitHub Actions workflow is defined in `.github/workflows/ci-cd.yml`
- It runs on every push to main branch
- It executes the same steps as local run but in a CI environment
- Docker image is built and pushed to Docker Hub (requires secrets setup)