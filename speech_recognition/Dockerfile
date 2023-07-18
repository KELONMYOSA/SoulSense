FROM python
RUN apt-get update && apt-get install -y ffmpeg
RUN wget https://huggingface.co/ggerganov/whisper.cpp/resolve/main/ggml-medium.bin
COPY ggml-medium.bin /root/.local/share/pywhispercpp/models/ggml-medium.bin
RUN git clone https://github.com/KELONMYOSA/soulsense_speech2text.git
WORKDIR soulsense_speech2text
COPY .env .env
EXPOSE 8000
RUN pip install -r requirements.txt
CMD ["python", "-m", "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]