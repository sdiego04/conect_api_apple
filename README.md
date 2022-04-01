# conect_api_apple

## Como gerar token de acesso as API'S da Apple utilizando PHP

1 - Você tem que ter cadastro na conta de desenvolvedor da Apple, caso não tenha este é o link https://appstoreconnect.apple.com/, se ja tiver vamos em frente.

2 - Após acessar a sua conta de desenvolvedor entre em Usuários e Acesso.

![](/assets/git2.JPG)

3 - Aqui você ira criar usa ISSUE, seu ID e apos deverá baixar um JSON(c) com essas informações que o próprio site disponibiliza

![](/assets/git1.jpg)

4 - Tendo em mãos o ISSUE, ID e JSON(Auth_XXXXXXXX.p8), precisamos ir na aba TestFlight e copiar nosso codigo na url, esse codigo fica exatamente onde esta o traçado preto na imagem abaixo.

![](/assets/git3.jpg)

5 - Apos termos todas as informações vamos baixar as blibliotecas, primeiro vamos baixar a JWT que é o padrão utilizado pela Apple https://jwt.io/libraries?language=PHP

6 - De acordo com a documentação da Apple o protocolo usado foi o ES256, então teremos que usar uma biblioteca que atenta os requisitos, nesse artigo utilizamos essa https://github.com/firebase/php-jwt que esta na versão 6.1.0, mas você pode usar o composer.

composer require firebase/php-jwt

7 - Importe a biblioteca para dentro do seu arquivo

![](/assets/git4.JPG)

8 - Agora vamos passar os parametros que pegamos no site da Apple e vamos passar para as variaveis, esse é o corpo das ulr's https://api.appstoreconnect.apple.com/v1/, que da acesso as API'S da Apple, para acessar qualquer API, basta contatenar o serviço com a url.


![](/assets/git5.JPG)