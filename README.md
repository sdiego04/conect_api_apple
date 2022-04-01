# conect_api_apple

## Como gerar token de acesso as API'S da Apple utilizando PHP

1 - Você tem que ter cadastro na conta de desenvolvedor da Apple, caso não tenha este é o link https://appstoreconnect.apple.com/, se ja tiver vamos em frente.

2 - Após acessar a sua conta de desenvolvedor entre em Usuários e Acesso.

![](/assets/git2.JPG)

3 - Aqui você ira criar usa ISSUE, seu ID e apos deverá baixar um JSON(c) com essas informações que o próprio site disponibiliza

![](/assets/git1.JPG)

4 - Tendo em mãos o ISSUE, ID e JSON(Auth_XXXXXXXX.p8), precisamos ir na aba TestFlight e copiar nosso codigo na url, esse codigo fica exatamente onde esta o traçado preto na imagem abaixo.

![](/assets/git3.JPG)

5 - Apos termos todas as informações vamos baixar as blibliotecas, primeiro vamos baixar a JWT que é o padrão utilizado pela Apple https://jwt.io/libraries?language=PHP

6 - de acordo com a documentação da Apple o protocolo usado foi o ES256, então teremos que usar uma biblioteca que atenta os requisitos, nesse artigo utilizamos essa https://github.com/firebase/php-jwt

composer require firebase/php-jwt

