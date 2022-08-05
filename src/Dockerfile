# Imagem base (por boa prática, usar imagens oficiais/confiáveis e com versão [para garantir a idempotência na instalação])
FROM node:16.16.0
# Diretório de trabalho (onde a aplicação será armazenada)
WORKDIR /app
# Baixar as bibliotecas de dependência do projeto (em package.json e package-lock.json)
# para o diretório corrente (./) = ./app
COPY ./package*.json ./
# Executar o gerenciador de pacotesdo Node para instalar as bibliotecas acima
RUN npm install
# Copia o restante dos arquivos do projeto
COPY . .
# Como a aplicação expõe a porta 8080, preciso fazer isso tb na máquina onde o app será instalado
EXPOSE 8080
# Executar a aplicação
CMD ["node", "server.js"]
