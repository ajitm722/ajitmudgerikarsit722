# backend/product_service/Dockerfile
FROM python:3.11-slim

WORKDIR /app

# Install runtime deps first (better layer cache)
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

# Copy app code
COPY app /app/app

# Runtime defaults
ENV PYTHONUNBUFFERED=1
EXPOSE 8000

# Start FastAPI app
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
