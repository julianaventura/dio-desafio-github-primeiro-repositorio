### Criando Chave SSH GitHub

A **chave SSH** é composta por duas chaves, sendo uma publica e uma privada. a chave publica é utilizada pelo destino e a chave privada com a máquina de criação da chave.

Pelo ***Git Bash***, digitar o comando:

- **ssh-keygen -t ed25519 -C "email** (de preferencia, o mesmo email usado no github)"

de enter e irá solicitar uma senha

- crie sua senha 

Após esse processo as chaves serão criadas. Para verificar as chaves, navegue até a pasta **.ssh**

- **cd /c/Users/"seu ususário"/.ssh/**
  - digite **ls** para listar 
    - as chaves serão listas 

Dentro da mesma pasta, digite o seguinte comando:

- **cat id_ed25519.pub** (.pub é a chave publica)
  - este comando irá gerar um link da sua chave publica
  - copie esse link e acesse seu ***GitHub***

Dentro da sua plataforma do ***GitHub*** acesse seu perfil, clicando na sua foto e localize ***SSH and GPG Keys***

- clique em **New SSH key**
  - no campo ***Title*** de nome a sua chave SSH, como por exemplo "Máquina Windows Casa"
  - no campo ***key***, cole o link copiado do ***Git Bash***
  - clique em ***Add SSH key***

Pronto, sua chave foi adicionada ao ***GitHub***



Volte para o ***Git Bash*** para iniciar a chave 

- Verifique se você esta na pasta **.ssh**
- digite o comando **eval $(ssh-agente -s)**
- este comando ira gerar o *Agente pid* (os números podem variar)
- para entregar o caminho da chave SSH digite o comando **ssh-add id_ed25519**





#### Pronto! Sua chave foi devidamente cadastrada e iniciada!

