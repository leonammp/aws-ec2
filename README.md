# Entrar nas Instâncias do AWS EC2

## 1. PRÉ REQUISITOS

- **"jq"**
```bash
sudo apt install jq
```

## 2. CONFIGURAÇÃO

#### 2.1 Configuração de certificado
Para entrar nas instâncias do EC2 é preciso colocar o seu certificado do EC2 na pasta **~/.ssh/**

Depois, no inicio do código do arquivo **"ec2"** vc pode alterar o nome do arquivo:
```bash
#!/bin/bash

# Nome do arquivo do certificado (dentro da pasta ~/.ssh/)
certificado_ssh=<COLOQUE AQUI O NOME DO CERTIFICADO> # Exemplo: certificado_ssh=portal-de-boletos-prod.pem
```

#### 2.2 Configuração de script bash
Se o arquivo **"ec2"** não estiver com permissão de execução:
```bash
sudo chmod +x ec2
```

Para executar o script em qualquer pasta do terminal vamos adicioná-lo na pasta **/usr/local/bin/**
```bash
sudo cp ec2 /usr/local/bin/
```

## 3. EXECUÇÃO
Após concluir a configuração, execute o comando sempre que precisar entrar nas instâncias do AWS EC2
```
ec2
```
