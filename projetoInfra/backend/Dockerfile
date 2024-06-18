#imagem base do Python
FROM python:3.9

#diretório de trabalho
WORKDIR /app

#instale as dependências
COPY requirements.txt .
RUN pip install -r requirements.txt

#Copie o código da aplicação
COPY app /app

#Exponha a porta 5000
EXPOSE 5000

#Comando para iniciar a aplicação
CMD ["python", "main.py"]
