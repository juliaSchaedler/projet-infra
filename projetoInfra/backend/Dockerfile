FROM python:3.9-slim

# Diretório de trabalho
WORKDIR /app

# Copia os arquivos de requisitos
COPY requirements.txt requirements.txt

# Instala as dependências
RUN pip install -r requirements.txt

# Copia o código da aplicação
COPY app app

# Define a variável de ambiente para Flask
ENV FLASK_APP=app/main.py

# Comando para rodar a aplicação
CMD ["flask", "run", "--host=0.0.0.0"]
