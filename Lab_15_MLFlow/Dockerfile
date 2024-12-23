FROM python:3.9-slim

# Install dependencies
RUN apt-get update && apt-get install -y gcc libpq-dev && rm -rf /var/lib/apt/lists/*

# Install MLflow
RUN pip install --no-cache-dir mlflow

# Ensure PATH includes the correct binary locations
ENV PATH="/usr/local/bin:/root/.local/bin:$PATH"

# Expose MLflow's default port
EXPOSE 5000

# Start the MLflow server
CMD ["mlflow", "server", "--host", "0.0.0.0", "--port", "5000"]
