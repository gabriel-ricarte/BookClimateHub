# Use uma imagem oficial do Node.js como imagem base
FROM node:14

# Defina o diretório de trabalho no contêiner
WORKDIR /app

# Copie o arquivo package.json e package-lock.json (se disponível)
COPY package*.json /app/

# Instale o Angular CLI e as dependências do projeto
RUN npm install -g @angular/cli && npm install

# Copie os arquivos do projeto para o diretório de trabalho
COPY . /app

# Exponha a porta 4200
EXPOSE 4200

# Comando para iniciar a aplicação Angular (substituído por comando npm start)
CMD ["ng", "serve", "--host", "0.0.0.0"]