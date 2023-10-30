<div align='center'>
  <img src=https://images.unsplash.com/photo-1566207474742-de921626ad0c?auto=format&fit=crop&q=80&w=1470&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D alt="logo" width= height= />
  <h1>WordPress Codex</h1>
  <p>Configuração do WordPress para desenvolvedores avançados</p>
  <h4>
    <a href=https://www.alphaville.host/>Ver Demo</a><span> · </span><a href="https://github.com/EuVictorhfs/WordPress-Codex/blob/master/README.md"> Documentação </a><span> · </span><a href="https://github.com/EuVictorhfs/WordPress-Codex/issues"> Reportar Bug </a><span> · </span><a href="https://github.com/EuVictorhfs/WordPress-Codex/issues"> Solicitar Recurso</a></h4>
</div>

# :notebook_with_decorative_cover: Índice

- [Sobre este projeto](#star2-sobre-este-projeto)
- [Roadmap](#compass-roadmap)
- [Licença](#warning-licença)
- [Contato](#handshake-contato)

## :star2: Sobre este projeto

Este projeto é dedicado a entusiastas em programação segura e performática do WordPress que buscam os melhores resultados de performance, otimização, segurança e desempenho. Ele serve para adequar sites à conformidade LGPD[^4^][8], ajuda a obter os melhores resultados nos mecanismos de busca orgânico e patrocinado[^5^][18][^6^][19][^7^][20][^8^][21][^9^][22] com o menor custo por clique. Além disso, retém os visitantes e converte consideravelmente mais leads, devido à sua alta performance e velocidade. Este projeto também auxilia visitantes em conexões lentas como 2G e 3G, aumentando significativamente os resultados digitais.

### :dart: Características

- **Programação PHP Avançada**: Este projeto utiliza técnicas avançadas de programação PHP para garantir a melhor performance e segurança.
- **Otimização para Mecanismos de Busca**: Implementamos estratégias eficazes para obter os melhores resultados nos mecanismos de busca orgânico e patrocinado.
- **Conformidade LGPD**: O projeto segue as diretrizes da LGPD para garantir a privacidade e segurança dos dados dos usuários.
- **Alta Performance**: Otimizado para velocidade e performance, este projeto garante uma experiência de usuário suave mesmo em conexões lentas.

**Palavras-chave:** Otimizações do Oxygen Builder, Domínio sem cookies, CDN, Controle de Cache Persistente, Polítcas de cabeçalho de segurança, Segurança avançada do WordPress, Otimizações do LiteSpeed.

### :key: Configurando as variáveis de ambiente
Este projeto requer um servidor com configurações abaixo.

```
PHP 8.1.x
```

```
MySQL 10.6.x
```

```
OS CloudLinux 4.18.x
```

```
cPanel 114.x
```

```
LiteSpeed Web Server Enterprise
```

### Dependências

Este projeto depende dos seguintes plugins, temas e softwares:

```
WordPress 6.3.x
```

```
Oxygen Theme 4.x
```

```
LiteSpeed Cache Plugin 5.7.0.1
```

## :toolbox: Vamos começar

### Instalação do WordPress

A instalação do WordPress deverá estar localizada em um subdiretório na raiz `public_html` do seu servidor (utilizamos o subdiretório `/public_html/www/` neste caso de uso). É necessário que o WordPress esteja utilizando o protocolo `https://` e `www` forçado, evitando conteúdos mistos e devido a utilização futura dos subdomínios para servir os conteúdos estáticos e de mídia, por exemplo. Segue abaixo as configurações de configuração base do WordPress para novas instalações:

- **URL de instalação**: `https://www.domain.tld/`
- **Opção multisite**: Desabilitado (as configurações do wp-config.php não irão funcionar no caso de multisites).
- **Backups automatizados por Cron (opcional)**: 0 5 1,15 * 0
- **Raíz de instalação do WordPress**: `/public_html/` (recomendamos instalar na raíz e mover os arquivos conforme a documentação, para evitar conflitos não previstos nesta documentação.
- **Criação de subdomínios**: `https://cdn.domain.tld` redirecionado para a pasta `/public_html/cdn`, que servirá para alteração da pasta padrão Uploads dentro do diretório wp-content; `https://static.domain.tld` redirecionado para a pasta `/public_html/static`, que servirá para alteração da pasta padrão wp-content do diretório raíz do wordpress
- **Criação de subdomínios (opcionais)**: `https://assets.domain.tld` redirecionado para a pasta `/public_html/assets`, que poderá servir conteúdos como branding resources e/ou servir arquivos sem proteção de hotlinks; `https://painel.domain.tld`, que poderá servir para alteração do acesso padrão wp-admin do wordpress, aumentando a segurança; `https://blog.domain.tld`, que poderá servir para alteração do caminho padrão de acesso /blog do wordpress

## :compass: Roadmap

1. Clone este repositório.
2. Verifique as dependências (listadas acima).
3. Instale o WordPress.
4. Teste seu ambiente para comparação posterior dos resultados.
5. Reconfigure os arquivos com suas informações confidenciais e implemente as novas regras de código.
6. Verifique o roadmap e teste seu ambiente (veja a seção "Testes" abaixo).
7. Inicie o servidor.

* [ ] Instalação do WordPress
* [ ] Movendo arquivos de diretório
* [ ] Configurando a pasta private
* [ ] Configurando o wp-config.php
* [ ] Configurando o htaccess do domínio principal
* [ ] Criando novas zonas DNS
* [ ] Configurando os novos .htaccess dos subdomínios
* [ ] Testando os resultados

### :test_tube: Rodando os testes

GT Metrix
```bash
https://gtmetrix.com/
```

Security Headers
```bash
https://securityheaders.com/
```

PageSpeed Insights
```bash
https://pagespeed.web.dev/
```

Sucuri SiteCheck
```bash
https://sitecheck.sucuri.net/
```

## :warning: Licença
Veja o arquivo LICENSE.txt para mais informações.

## :handshake: Contato
Victor Hugo Ferreira - - victorhferreira@icloud.com
Link do projeto: [https://github.com/euvictorhfs/wordpress-codex/](https://github.com/euvictorhfs/wordpress-codex/)
