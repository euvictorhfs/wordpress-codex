# WordPress Codex

## Instruções de instalação do WordPress
O WordPress deverá ser instalado no diretório raiz da sua hospedagem, sem subdiretórios, utilizando protocolo 'https://' com 'www'. Após a instalação, mova todos os arquivos de instalação para um diretório próprio dentro de 'public_html', como a pasta 'public_html/www'. Copie (NÃO MOVA) os arquivos .htaccess e index.php para a raiz da hospedagem 'public_html'. Feito essas modificações, comece a editar o 'wp-config.php'.

## Informações do Servidor
* PHP 8.1.x
* MySQL 10.6.x
* WordPress 6.3.x
* OS CloudLinux 4.18.x
* cPanel 114.x

## Tema utilizado
* Oxygen Builder 4.x

## Plugin utilizado
* LiteSpeed Cache 5.7.0.1

## Informações de configuração do WordPress
* URL de instalação: https://www.domain.tld/
* Multisite: desabilitado
* Backups automatizados por Cron: 0 5 1,15 * 0
* Raíz de instalação do WordPress: '/public_html'

## Informações dos subdomínios criados
* https://cdn.domain.tld -> '/public_html/cdn'
* https://static.domain.tld -> '/public_html/static'

## Informações dos subdomínios opcionais criados
* https://assets.domain.tld -> '/public_html/assets'
* https://painel.domain.tld
* https://blog.domain.tld
