## Configurar chave ssh (Linux)

- ssh-keygen -t ed25519 -C seuemail@email.com 
- cd /home/user/.ssh   (linha para ir na pasta criada)
- cat id_ed25519.pub (em seguida adicione a chave no Github)
- eval $(ssh-agent -s)
- ssh-add id_ed25519

## Configurar Git

- git config --global user.email "seuemail@mail.com"
- git config --global user.name "username"

## Desconfigurar Git

- git config --global --unset user.email
- git config --global --unset user.name

## Criar, adicionar e commitar

- git init
- git add *  (para adicionar todos os arquivos)
- git commit -m "mensagem"