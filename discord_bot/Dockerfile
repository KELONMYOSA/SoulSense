FROM python
RUN apt-get update && apt-get install -y libffi-dev libnacl-dev opus-tools
RUN git clone https://github.com/KELONMYOSA/soulsense_discord_bot.git
WORKDIR soulsense_discord_bot
COPY .env .env
RUN pip install -r requirements.txt
CMD python nltk_download.py && python main.py