

mashup20192-modelo/osTicket- Criado por Gabriel
========
<a href="https://osticket.com"><img height="80px" width="80px" src="images/favicon.png"
align="left" hspace="10" vspace="6"></a>
**osTicket** é um sistema de ticket de suporte open-source.Ele faz a integração perfeita 
das consultas criadas por e-mail, telefone e formulários baseados na 
Web fazendo uso de uma interface web multiusuário simples e fácil de usar.
Gerencia, organiza e arquiva todas as suas solicitações e respostas de suporte em um só lugar, 
enquanto fornece clientes com responsabilidade e capacidade de resposta que merecem.


Como o osTicket funciona para você
--------------------------
  1. Os usuários criam tickets por meio de seu site, email ou telefone
  1. Os tickets recebidos são salvos e atribuídos aos agentes
  1. Os agentes ajudam seus usuários a resolver seus problemas



Dependências\Requisitos
------------
  * HTTP server running Microsoft® IIS or Apache
  * PHP version 7.0 to 7.3, 7.3 is recommended
  * mysqli extension for PHP
  * MySQL database version 5.5

### Recomendações
  * gd, gettext, imap, json, mbstring, and xml extensions for PHP
  * APC module enabled and configured for PHP

Instalação e Download
----------
	*sudo mkdir /var/www/html/osticket
	*cd /var/www/html/osticket
	*wget http://osticket.com/sites/default/files/download/osTicket-v1.10.zip
	*sudo unzip osTicket-v1.10.1.zip
	*sudo cp include/ost-sampleconfig.php include/ost-config.php

Para completar a instalação é necessário a criação de um banco de dados
para alocação da alicação, e os arquivos são adquiridos através do repositório
dos desenvolvedores da aplicação.
Configurar apache:

    sudo nano /etc/apache2/sites-available/osticket.conf


      <VirtualHost *:80>
	
		ServerAdmin admin@example.com		
		DocumentRoot /var/www/html/osticket
		ServerName example.com
		ServerAlias www.example.com

      <Directory /var/www/osticket/>
     
          Options FollowSymlinks
          AllowOverride All
          Require all granted
	  
      </Directory>

      ErrorLog ${APACHE_LOG_DIR}/error.log     
      CustomLog ${APACHE_LOG_DIR}/access.log combined
     
      </VirtualHost>

Em serverAdmin/ServerName/ServerAlias pode ser usado qualquer um a sua escolha

Após a instalação e download seguindo os passos anteriores vamos acessar
pelo navegador o seguinte endereço

	http:host/osTicket
Sendo host o hospedeiro que foi escolhido para o site, após isso iremos 
seguir os passos de instalação normalmente indicando o banco criado anteriormente
e configurações de administrador que são descritas nos formulários a seguir:

![ostciket_01](https://user-images.githubusercontent.com/57021668/77785686-4fa7cd80-703b-11ea-8745-9971cee01101.jpg)

![ostciket_02](https://user-images.githubusercontent.com/57021668/77785699-520a2780-703b-11ea-8082-e1ca44c64702.jpg)

![ostciket_03](https://user-images.githubusercontent.com/57021668/77785708-546c8180-703b-11ea-9f84-7900d3e2c487.jpg)

![ostciket_04](https://user-images.githubusercontent.com/57021668/77785716-559dae80-703b-11ea-8e12-5f55d1e5e41d.jpg)

![ostciket_05](https://user-images.githubusercontent.com/57021668/77785726-58989f00-703b-11ea-86e2-cec5f04c74c0.jpg)

![ostciket_06](https://user-images.githubusercontent.com/57021668/77785734-5afaf900-703b-11ea-9339-6cdfc104648d.jpg)


Teste
---------
O teste realizado está nas imagens a seguir, foi feita a criação de um novo ticket
em que foram incluidas imagens foi feito o uso do email gabrieljorro8@outlook.com
com a observação que esse email já possuí uma conta e por isso foi identificado com o nome
registrado aneteriormente, é importante salientar que a criação da conta para criar tickets não
é obrigatória, depois foi realizado login no administrador para verificar se o tópico tinha sido 
criado e a imagem adicionada.

	administrador:
	login : gabrieljorro5@gmail.com.br
	senha: gsc841998
	usuário: gabrielsc

![01](https://user-images.githubusercontent.com/57021668/78414374-29ad9a80-75f2-11ea-9a89-b5d25be70a77.PNG)

![02](https://user-images.githubusercontent.com/57021668/78414377-2b775e00-75f2-11ea-8a04-87e1fe88172d.PNG)

![03](https://user-images.githubusercontent.com/57021668/78414379-2d412180-75f2-11ea-87cb-c26ae4b3a9e2.PNG)

![04](https://user-images.githubusercontent.com/57021668/78414381-2dd9b800-75f2-11ea-88be-514984d996e1.PNG)

![05](https://user-images.githubusercontent.com/57021668/78414390-33370280-75f2-11ea-8077-4d1f24bed339.PNG)

![06](https://user-images.githubusercontent.com/57021668/78414392-3500c600-75f2-11ea-8942-eff8c91bd39d.PNG)

![07](https://user-images.githubusercontent.com/57021668/78414395-36ca8980-75f2-11ea-96b4-b114433bd5aa.PNG)

![08](https://user-images.githubusercontent.com/57021668/78414396-39c57a00-75f2-11ea-9cf5-1e1f6ea7e97c.PNG)

![09](https://user-images.githubusercontent.com/57021668/78414398-3af6a700-75f2-11ea-9d5e-1b6541da6506.PNG)

![10](https://user-images.githubusercontent.com/57021668/78414399-3cc06a80-75f2-11ea-9896-93d080e30898.PNG)

![11](https://user-images.githubusercontent.com/57021668/78414469-87da7d80-75f2-11ea-93ec-7aab25a1176b.PNG)
Para realizar o teste foi dado o comando (as 22:17 , as 20:57 e as 21:20 do dia 03/04/2020):

	*palemoon 172.17.0.1:2087/osticket

obs: foi executado tres vezes pois a interface web estava travada e impossibilitava o teste

Licença
-------
osTicket é liberado pela licensa GPL2. Os detalhes sobre a licença estão
no arquivo LICENSE.txt.
* https://github.com/DCOMP-UFS/mashup20192-mashup-aurora/blob/master/osTicket/LICENSE.txt

o osTicket é suportado por vários projetos de código aberto, incluindo:

  * [Font-Awesome](http://fortawesome.github.com/Font-Awesome/)
  * [HTMLawed](http://www.bioinformatics.org/phplabware/internal_utilities/htmLawed)
  * [jQuery dropdown](http://labs.abeautifulsite.net/jquery-dropdown/)
  * [jsTimezoneDetect](http://pellepim.bitbucket.org/jstz/)
  * [mPDF](http://www.mpdf1.com/)
  * [PasswordHash](http://www.openwall.com/phpass/)
  * [PEAR](http://pear.php.net/package/PEAR)
  * [PEAR/Auth_SASL](http://pear.php.net/package/Auth_SASL)
  * [PEAR/Mail](http://pear.php.net/package/mail)
  * [PEAR/Net_SMTP](http://pear.php.net/package/Net_SMTP)
  * [PEAR/Net_Socket](http://pear.php.net/package/Net_Socket)
  * [PEAR/Serivces_JSON](http://pear.php.net/package/Services_JSON)
  * [php-gettext](https://launchpad.net/php-gettext/)
  * [phpseclib](http://phpseclib.sourceforge.net/)
  * [Spyc](http://github.com/mustangostang/spyc)
