# Entrar nas Instâncias do AWS EC2

## 1. CONFIGURAÇÃO

#### 1.1 Configuração de certificado
Para entrar nas instâncias do EC2 é preciso colocar o seu certificado do EC2 na pasta **~/.ssh/**

Depois, no inicio do código do arquivo **"ec2"** vc pode alterar o nome do arquivo:
```bash
#!/bin/bash

# Nome do arquivo do certificado (dentro da pasta ~/.ssh/)
certificado_ssh=<COLOQUE AQUI O NOME DO CERTIFICADO> # Exemplo: certificado_ssh=meu_certificado.pem
```

#### 1.2 Configuração de script bash
Se o arquivo **"ec2"** não estiver com permissão de execução:
```bash
sudo chmod +x ec2
```

Para executar o script em qualquer pasta do terminal vamos adicioná-lo na pasta **/usr/local/bin/**
```bash
sudo cp ec2 /usr/local/bin/
```

## 2. EXECUÇÃO
Após concluir a configuração, execute o comando sempre que precisar entrar nas instâncias do AWS EC2.

Por padrão a região da aws está configurada como **"sa-east-1"** no arquivo. Se você quiser utilizar a região padrão basta executar:
```bash
ec2
```

Se quiser mudar a região, é possível passar como parâmetro:
```bash
ec2 us-east-1
```
