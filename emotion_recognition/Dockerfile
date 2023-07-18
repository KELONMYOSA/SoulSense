FROM python
RUN git clone https://github.com/KELONMYOSA/soulsense_emotion_recognition.git
WORKDIR soulsense_emotion_recognition
EXPOSE 7000
RUN pip install torch --index-url https://download.pytorch.org/whl/cu118
RUN pip install -r requirements.txt
CMD ["python", "-m", "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "7000"]