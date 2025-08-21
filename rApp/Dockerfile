FROM python:3.12-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY rapp.py /app/
ENV PYTHONUNBUFFERED=1
EXPOSE 8080
CMD ["python","-m","uvicorn","--app-dir","/app","rapp:app","--host","0.0.0.0","--port","8080"]
