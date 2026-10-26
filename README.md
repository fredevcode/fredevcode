<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img alt="Frédéric Navez — Machine Learning Engineer · MLOps" src="assets/header-light.svg" width="100%">
</picture>

<p>
  <a href="https://fredevcode.dev/"><img alt="Website" src="https://img.shields.io/badge/fredevcode.dev-1f2328?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
  <a href="https://www.linkedin.com/in/fredericnavez/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="https://x.com/fredevcode"><img alt="X" src="https://img.shields.io/badge/@fredevcode-000000?style=for-the-badge&logo=x&logoColor=white"></a>
</p>

I'm a **Machine Learning Engineer** who takes models past the notebook: reliable data pipelines, reproducible training, and services that run in production.
Before ML, I was a **biology engineer** — I still work like a scientist: clear hypotheses, honest evaluation, results you can reproduce.

## Focus

| Area | What I do |
|---|---|
| **Data pipelines** | Collection, cleaning and feature engineering as versioned, scheduled jobs |
| **Modelling** | Classical ML and NLP, with evaluation that reflects the real use case |
| **Serving** | Secure REST APIs around models, with logging and a lightweight UI |
| **MLOps** | Containerised workflows, CI/CD and automated retraining on fresh data |

## Featured work

### [Sentiment Analysis — end-to-end MLOps](https://github.com/fredevcode/MLOps_SentimentAnalysis)

A production-style system that scrapes Trustpilot reviews, retrains a sentiment model on schedule and serves predictions behind an authenticated API.

```mermaid
flowchart LR
    A[Trustpilot] -->|scraping job| B[(S3 raw)]
    B -->|preprocessing job| C[(S3 processed)]
    C -->|retraining job| D[Model + score]
    D --> E[FastAPI<br/>OAuth2 · JWT]
    E --> F[Streamlit UI]
```

- **4 independent Docker jobs** — scraping, preprocessing, retraining and API — each triggered by its own GitHub Actions workflow
- **Automated retraining** on reviews stored in S3, with the model score saved alongside each version
- **Continuous delivery** — the API image is built, pushed to Docker Hub and deployed on every release
- **Stack** — Python · scikit-learn · NLTK · pandas · FastAPI · Streamlit · Docker · AWS S3

## Tech stack

<p>
  <img alt="Python, scikit-learn, FastAPI, Docker, AWS, GitHub Actions, Linux, Bash, Git, TypeScript, React, Next.js" src="https://skillicons.dev/icons?i=python,sklearn,fastapi,docker,aws,githubactions,linux,bash,git,ts,react,nextjs&perline=12">
</p>

- **ML & data** — Python, scikit-learn, pandas, NumPy, NLTK, SQL
- **Serving** — FastAPI, Streamlit, REST
- **MLOps & infra** — Docker, docker-compose, GitHub Actions, AWS S3, Linux
- **Product** — TypeScript, React, Next.js

## Get in touch

Happy to talk about ML engineering, MLOps or a project you're building.
The fastest way to reach me is [LinkedIn](https://www.linkedin.com/in/fredericnavez/).
