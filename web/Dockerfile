FROM python:3.12-slim
WORKDIR /app
COPY server.py search_core.py check_links.py start.sh ./
COPY static/ ./static/
ENV JUICEPANS_HOST=0.0.0.0
ENV JUICEPANS_PORT=8765
ENV PYTHONUNBUFFERED=1
EXPOSE 8765
CMD ["python3", "server.py"]
