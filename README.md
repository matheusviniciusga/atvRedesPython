# Atividade Chat Via Socket
- Disciplina: Redes de Computadores
- Prof.: Daniel Bezerra

# Integrantes
- Matheus Vinícius G. de Andrade
- Maria Cecília Sitcovsky
-------------------------------------------------------------

## Introdução
a

### Servidor
a

#### Cabeçalho
O cabeçalho é definido em 64 "bytes", representando o tamanho que cada mensagem precisa possuir ao ser enviada a um servidor.
#### Endereço Local IP
Para descobrir o endereço IP da sua máquina, digite no cmd 'ipconfig' e no protocolo IPV4 é onde estará o seu IP, ou use o segundo script para obter automaticamente oseu IP.
~~~Python
SERVER = "127.0.0.1"
SERVER = socket.gethostbyname(socket.gethostname())
~~~
#### Outras Configurações
b
#### Indicando a Conexão Específica
b
#### Conexão Cliente-Servidor
b
#### Função para Iniciar o Servidor
b

-------------------------------------------------------------
### Cliente
a

#### Função de Mandar Mensagem
b
