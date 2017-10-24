Instalação
==========

Modo local
----------

  É interessante primeiro testar localmente, sem ter que enviá-las para um servidor remoto toda a vez, para isso, você pode instalar o WordPress localmente.

  Existem aplicativos que podemos baixar e configurar para executar um web site em nosso próprio computador.

  Esse programas servem para criar servidores independente da plataforma e consistem principalmente na base de dados MySQL, o servidor web Apache e os interpretadores para linguagens de script: PHP e Perl, além do WordPress, você poderá instalar qualquer software que use estas linguagens.

  * `XAMPP <http://www.apachefriends.org/pt_br/xampp-windows.html>`_.
  * `WAMP <http://www.profissionaisti.com.br/2012/03/instalando-apache-php-mysql-no-windows-com-wamp/>`_.
  * `MAMP <http://www.profissionaisti.com.br/2012/04/instalando-apache-php-mysql-no-mac-os-com-mamp/>`_ (para Mac).
    
  no meu caso, eu utilizei o WAMP, pois com alguns poucos passos, ele começou a funcionar.


  Passo a passo:

  * faça o download do `WAMP <http://www.profissionaisti.com.br/2012/03/instalando-apache-php-mysql-no-windows-com-wamp/>`_.
  * configure o arquivo php.ini no diretório:  ``C:wamp64\bin\apache\apache2.4.27\bin`` (onde normalmente fica instalado)
  * Abra o arquivo php.ini no bloco de notas ou qlqr outro editor
      * edite as variáveis: memory_limit = 128M e upload_max_sizing = 2M para **750M**
      * salvar
  * Start o Wampserver,
  * Digite no browser localhost e aperte enter,
  * Baixe o zip WordPress  no site oficial em seguida recorte e cole no diretório: C:\wamp64\www
  * Extraia os arquivos baixados dentro do diretorio **www** 
  * Renomeie de acordo com o nome do seu site,
  * Acesse localhost/phpmyadmin/
  * crie um banco de dados (preferência com o mesmo nome que do seu site)
  * Acesse pelo o browser **localhost/nome da pasta do seu site/**
  * Será direcionado para página de instalação do WordPress
      - digite o nome do banco de dados criado anteriormente
      - digite o usuario: por padrão é root
      - o campo de senha: deixe em branco
      - servidor do bd: localhost
      - prefixo da tabela: wp
        
  * clique em enviar, depois instalar, pronto!
  
  Depois disso basta escolher usuário, senha e email para poder acessar. 


WordPress local para Site Web
-----------------------------

  Após ter criado um site local, é possível importá-lo para um site web, os passos são os mesmo de importar o WordPress entre servidores:

  Instale o WordPress no seu servidor web, pode ser manualmente ou através das ferramentas do serviço de hospedagem, geralmente você pode escolher entre instalar na raiz do site ou em uma pasta blog ou site.
  
  Usando um cliente FTP ou o gerenciador de arquivos do serviço de hospedagem, exclua a pasta **wp-content** da instalação web e em seguida envie a mesma pasta da sua instalação local. Isso vai manter seu tema e plugins.
  
  No servidor web, crie um banco de dados vazio com o mesmo nome e senha do banco de dados local, estas informções ficam no arquivo **wp-config.php**.
  
  Exporte os dados do banco de dados local, de preferência em formato *.zip*.
  
  Importe o arquivo .zip em seu banco de dados web.
  
  Acesse a tabela com sufixo **</tt>_options</tt>** e mude os **URLs** em **siteurl** e home para o URL de seu site web.
  
  Tente acessar seu site e observe se consegue acessar os links normamente no site.





