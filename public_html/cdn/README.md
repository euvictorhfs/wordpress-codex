# Configuração de domínio livre de cookies para servir conteúdo estático
Este código é um arquivo de configuração do servidor web Apache para o site "alphaville.host". Ele define as configurações de segurança, cache, redirecionamento e otimização do site para um domínio livre de cookies.

## Segurança
* Desabilita todos os cookies
* Protege contra ataques de clickjacking
* Protege contra ataques de XSS
* Protege contra ataques de MIME sniffing
* Protege contra ataques de downgrade
## Cache
* Habilita o CORS para todos os arquivos estáticos
* Habilita o cache de navegador para todos os arquivos estáticos por 1 ano
* Desabilita o cache de navegador para arquivos dinâmicos
## Redirecionamento
* Redireciona todas as solicitações para o domínio principal, www.alphaville.host
## Otimização
* Habilita o cache HTTP para todos os arquivos estáticos
