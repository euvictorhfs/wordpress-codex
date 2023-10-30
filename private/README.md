# Como proteger os arquivos base do WordPress

Os arquivos base do WordPress contêm informações importantes, como a senha do banco de dados e as chaves secretas. É importante proteger esses arquivos para evitar que eles sejam acessados por invasores.

Para proteger os arquivos base do WordPress, siga estas etapas:

1. **Copie as informações confidenciais do arquivo wp-config.php.** Essas informações incluem informações sobre o banco de dados, as chaves secretas e o modo de depuração do WordPress.
2. **Crie uma pasta privada para armazenar as informações confidenciais.** Essa pasta deve ser protegida por senha ou por um firewall e não poderá estar no diretório `/home/public_html/www`. A pasta deverá ficar na raíz do servidor `/home/private`.
3. **Crie três arquivos PHP na pasta privada.** Esses arquivos armazenarão as informações confidenciais.
4. **Proteja os arquivos.** Para proteger os arquivos, você pode definir as permissões de arquivo para 600 ou 400. Isso impedirá que usuários não autorizados acessem o arquivo.
5. **Cole as informações copiadas do arquivo `wp-config.php` separadas em cada novo arquivo.** Isso permitirá que, após o salvamento, você possa remover as informações do `wp-config.php` e carregar todas as informações confidenciais de forma protegida.
6. **Você também pode usar a ferramenta de criptografia com o OpenSSL para criptografar os arquivos.** 

Ou seja, seu arquivo wp-config.php possuirá somente as informações:

```php
<?php
/**#@-*/

/** Absolute path to the WordPress directory. */
if ( ! defined( 'ABSPATH' ) ) {
	define( 'ABSPATH', __DIR__ . '/' );
}

/** Sets up WordPress vars and included files. */
require_once ABSPATH . 'wp-settings.php';
?>
```

> **Atenção**: Copie as informações e salve-as em um bloco de notas. Ela contem as informações de instalação do seu WordPress e, em caso de perda, você poderá quebrar seu site. Não remova as informações antes de copia-las corretamente.



## Como proteger as informações do banco de dados do WordPress

@see [database.php](https://github.com/euvictorhfs/wordpress-codex/blob/main/private/database.php)

O arquivo `database.php` do WordPress contém informações confidenciais sobre o banco de dados do site, como o nome do banco de dados, o usuário do banco de dados e a senha do banco de dados. É importante proteger essas informações para evitar que elas sejam acessados por invasores.

1. **Crie um arquivo `database.php` na pasta privada dentro do diretório `/home/private`.**
2. **Cole neste arquivo todas as informações copiadas do `wp-config.php` referentes ao banco de dados.** Essas informações incluem o DB_NAME, DB_USER, DB_PASSWORD, DB_HOST, DB_CHARSET, DB_COLLATE e $table_prefix.
3. **Retorne ao arquivo `wp-config.php` e insira a requisição do arquivo `database.php`.** Depois de proteger o banco de dados, você pode adicioná-los ao arquivo `wp-config.php` usando o comando `require()`. O código está ao final deste documento para referência.

Após seguir essas etapas, as informações do banco de dados do WordPress serão armazenadas em um arquivo seguro e protegido.



## Como proteger as chaves secretas do WordPress

@see [secret-keys.php](https://github.com/euvictorhfs/wordpress-codex/blob/main/private/secret-keys.php)

As chaves secretas do WordPress são usadas para gerar tokens de autenticação usados para proteger o login dos usuários e outras atividades no site. É importante que essas frases sejam únicas e seguras.

Para proteger as chaves secretas do WordPress, siga estas etapas:

1. **Crie um arquivo `secret-keys.php` na pasta privada dentro do diretório `/home/private`.**
2. **Cole neste arquivo todas as informações copiadas do `wp-config.php` referentes as chaves secretas.** Essas informações incluem a chave secreta do AUTH_KEY, a chave secreta do SECURE_AUTH_KEY, a chave secreta do LOGGED_IN_KEY, a chave secreta do NONCE_KEY e a chave secreta do AUTH_SALT.
3. **Retorne ao arquivo `wp-config.php`, remova as informações das cahves secretas copiadas e adicione a linha de requisição do arquivo `secret-keys.php`.** Depois de proteger as chaves secretas, você pode adicioná-los ao arquivo `wp-config.php` usando o comando `require()`. O código está ao final deste documento para referência.

Após seguir essas etapas, as chaves secretas do WordPress serão armazenadas em um arquivo seguro e protegido.

* Para gerar as chaves secretas, você pode usar o seguinte comando:

```
wp secret-keys
```

O comando acima gerará cinco frases secretas que você pode copiar e colar no arquivo `secret-keys.php`.

**Essa última etapa pode ajudar a proteger seu site Wordpress de ataques.**



## Como proteger o modo de depuração do WordPress

@see [debug.php](https://github.com/euvictorhfs/wordpress-codex/blob/main/private/debug.php)

O modo de depuração do WordPress é uma ferramenta de desenvolvimento que permite visualizar informações de depuração no site. No entanto, o modo de depuração também pode expor informações confidenciais, como senhas e chaves secretas.

Desative o modo de depuração quando não estiver usando-o. O modo de depuração está ativado por padrão no WordPress em alguns casos. Isolar este arquivo proteger contra invasores usarem a senha do banco de dados, chave secreta ou erros e mensagens de aviso para identificar vulnerabilidades no seu site.

Para proteger as variáveis de ambiente para depuração do WordPress, siga estas etapas:

1. **Crie um arquivo `debug.php` na pasta privada dentro do diretório `/home/private`.**
2. **Cole neste arquivo todas as informações copiadas do `wp-config.php` referentes ao modo de depuração.** Essas informações incluem o WP_DEBUG.
3. **Retorne ao arquivo `wp-config.php`, remova as informações do debug copiadas e adicione a linha de requisição do arquivo `debug.php`.** Depois de proteger o modo de depuração, você pode adicioná-los ao arquivo `wp-config.php` usando o comando `require()`. O código está ao final deste documento para referência.



## Exemplo de inserção no wp-config.php

@see  [wp-config.php](https://github.com/euvictorhfs/wordpress-codex/blob/main/public_html/www/wp-config.php)

```php
// Carrega as chaves secretas
require_once(dirname(__FILE__) . '/../private/secret-keys.php');

// Carrega as informações do banco de dados
require_once(dirname(__FILE__) . '/../private/database.php');

// Carrega as variáveis de depuração
require_once(dirname(__FILE__) . '/../private/debug.php');
```

## Contribuições

Se você tiver algum feedback ou sugestão sobre o texto ou o código, por favor, deixe um comentário no GitHub. Seu feedback é importante para melhorar este guia.

Se você quiser contribuir para este guia, você pode fazer um fork do repositório no GitHub e enviar uma pull request.

Agradecemos sua leitura. Esperamos que este guia tenha sido útil.
