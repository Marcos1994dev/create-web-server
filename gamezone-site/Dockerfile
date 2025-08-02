# Usa imagem leve do nginx para servir seu site estático
FROM nginx:alpine

# Remove arquivos padrões do nginx
RUN rm -rf /usr/share/nginx/html/*

# Copia seus arquivos HTML para a pasta padrão do nginx
COPY . /usr/share/nginx/html

# Expõe a porta 80 para acessar o site
EXPOSE 80
