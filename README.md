### emotivice 设置
1.停止容器
2.
docker run -d --name emotivoice ^
  -p 127.0.0.1:8509:8501 ^
  -p 127.0.0.1:8000:8000 ^
  syq163/emoti-voice:latest
3.docker exec -it emotivoice bash 进入容器
4.在容器里
uvicorn openaiapi:app --host 0.0.0.0 --port 8000

配置文件设置
[emotivoice]
base_url = "http://host.docker.internal:8000"
model = "emoti-voice"