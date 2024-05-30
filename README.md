# Atividade Chat Via Socket
- Disciplina: Redes de Computadores
- Prof.: Daniel Bezerra

# Integrantes
- Matheus Vinícius G. de Andrade
- Maria Cecília Sitcovsky
-------------------------------------------------------------

## Introdução
Prpjeto simples de comunicação entre usuários via "socket" por um servidor, executando funções simultaneamente através dos "threads".

### Servidor
Abaixo estará as configurações de um servidor que pode receber vários clientes e administrar a sua comunicação e troca de dados entre eles.

#### Cabeçalho
O cabeçalho é definido em 64 "bytes", representando o tamanho que cada mensagem precisa possuir ao ser enviada a um servidor.
#### Endereço Local IP
Para descobrir o endereço IP da sua máquina, digite no cmd `ipconfig` e no protocolo IPV4 é onde estará o seu IP, ou use o segundo script para obter automaticamente o seu IP.
~~~
SERVER = "127.0.0.1"
SERVER = socket.gethostbyname(socket.gethostname())
~~~
#### Outras Configurações
* ADDR serve para vincular o soquete, em forma de tupla, ao servidor que possuia informações dos protocolos IPV4(endereço IP da máquina) e porta de comunicação do servidor;
* Sempre ao enviar uma mensagem, ela precisa ser codificada em formato `UTF-8`, para que o usuário possa entender a mensagem;
* Definimos uma forma de como um cliente posssa se desconectar com o servidor de forma "amigável".
* Criamos uma lista de clientes, para que o servidor possa suportar vários clientes e administrar quem vai enviar a mensagem e recebe-lá
~~~
ADDR = (SERVER, PORT)
FORMAT = 'UTF-8'
DISCONNECT_MESSAGE = "Desconectar"
clients = []
~~~
#### Indicando a Conexão Específica
* Vinculamos ao servidor, um tipo específico de soquete, `SOCK_STREAM` (que indica oprotocolo TCP que será usado nas transmissões das mensagens);
* Colocamos a conexão do servidor em um bloco `try-catch`, para tratar uma exceção caso venha acontecer durante a inicialização do servidor;
~~~
server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
try:
    server.bind(ADDR)
    print('Servidor Iniciado...')
except:
    print('Servidor não foi inicializado.')
~~~
#### Conexão Cliente-Servidor
Função que lidará com as multiplas conexões dentro do servidor de forma simultânea, em sua própria "thread".
~~~
def tratarCliente(client, addr):
    //código aqui...
~~~
* Aqui, mostramos que uma nova conexão foi estabelecida no servidor e o endereço do cliente que se conectou
* Ao conectar, dizemos que a conexão com o servidor é verdadeira e colocamos o cliente conectado na lista de clientes do servidor
~~~
print(f"[NOVA CONEXÃO] {addr} conectado.")
conectado = True
clients.append(client)
~~~
* Enquanto a conexão é verdadeira, tentamos em um bloco `try-catch`, receber a mensagem de um cliente, pegando o tamanho real da mensgaem...
#### Função para Mandar a Mensagem à Todos Conectados
b
#### Função que Remove o Cliente da Lista
b
#### Função para Iniciar o Servidor
b

-------------------------------------------------------------
### Cliente
a

#### Função de Mandar Mensagem
b
