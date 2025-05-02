# flask_app_pipeline
# Flask App Deployment with Docker, GitHub Actions, and AWS

This project demonstrates how to containerize a Flask application using Docker, automate the CI/CD pipeline with GitHub Actions, and deploy it to an AWS EC2 instance.

## 🚀 Tech Stack

- **Flask** – Lightweight Python web framework
- **Docker** – Containerization
- **GitHub Actions** – CI/CD pipeline automation
- **AWS EC2** – Cloud hosting

## 📁 Project Structure

.
├── app/ # Flask app files
│ └── app.py
├── Dockerfile # Docker configuration
├── .github/workflows/
│ └── deploy.yml # GitHub Actions workflow
├── requirements.txt
└── README.md

bash
Copy
Edit

## ⚙️ Setup & Run Locally

```bash
# Clone the repo
git clone https://github.com/your-username/flask-docker-aws-cicd.git
cd flask-docker-aws-cicd

# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run locally
python app/app.py
🐳 Build & Run with Docker
bash
Copy
Edit
docker build -t flask-app .
docker run -p 5000:5000 flask-app
🔁 CI/CD with GitHub Actions
The deploy.yml workflow:

Builds the Docker image

Connects to your AWS EC2 instance via SSH

Pulls the latest code and restarts the container

Make sure your secrets (AWS_HOST, AWS_USER, SSH_KEY) are set up in your GitHub repository under Settings > Secrets.
👉  [Read the full guide on Medium]([https://medium.com/@your-profile/your-article-link](https://medium.com/@muktimishra_16596/from-hello-world-to-production-deploying-a-flask-app-with-docker-aws-ecs-github-actions-91b37dac15aa))
