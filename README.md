# Hostinger ssl com getssl (https://github.com/srvrco/getssl)

#### 1. Rodar o seguinte comando para gerar os arquivos em .getssl
```sh
./getssl -c nome_do_dominio
```

#### 2. Para habilitar o servidor de produção basta descomentar a linha 13
```sh
CA="https://acme-v02.api.letsencrypt.org"
```

#### 3. Alterar o ACL para a pasta acme-challenge do dominio
```sh
ACL=('/home/user/public_html/.well-known/acme-challenge/')
```

#### 4. Alterar a opção USE_SINGLE_ACL para true
```sh
USE_SINGLE_ACL="true"
```

#### 5. Rodar o seguinte comando para gerar os arquivos ssl (certificado, chave e bundle)
```sh
./getssl nome_do_dominio
```

#### TODO: Estudar uma forma de atualizar automaticamente sem precisar abrir a interface e copiar os arquivos para lá
