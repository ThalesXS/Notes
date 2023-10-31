## *Uncomplicated Firewall* (UFW)
&nbsp; *Uncomplicated Firewall* é um programa para gerenciar *netfilter firewall* de forma fácil e prática através da linha de comandos.

### Comandos UFW.
&nbsp; O UFW usa o [CLI](Linux\1.%20Command%20Line%20Interface.md) para gerenciar de forma conveniente o *firewall*.

#### Estado
<br>

- *`ufw status`*
>&nbsp; Indica se o *Firewall* se encontra ativo ou não, bem como informações relativas a regras criadas.

- *`ufw status numbered`*
>&nbsp; Similar a opção anterior, porém passa a enumerar as regras criadas.

#### Ativar e Desativar
<br>

- *`ufw enable`*
>&nbsp; Caso o UFW esteja desativado, irá ativar o mesmo.

- *`ufw disable`*
>&nbsp; Caso o UFW esteja ativado, irá desativar o mesmo.


#### Gerenciando Portas
<br>

- *`ufw allow <port>/<protocol>`*
>&nbsp; Permite a entrada de pacotes que façam uso do protocolo designado na porta descrita, caso nenhum protocolo seja designado, todos serão aceitos pela porta.
>
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw allow 42`*
>>&nbsp; Permite a entrada de pacotes pela porta 42.
>
>- *`ufw allow 42/tcp`*
>>&nbsp; Apenas os pacotes de protocolo TCP serão aceitos na porta 42.

</details>

- *`ufw deny <port>/<protocol>`*
>&nbsp; Bloqueia a entrada de pacotes que façam uso do protocolo designado na porta descrita, caso nenhum protocolo seja designado, todos serão bloqueados pela porta.
>
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw deny 53`*
>>&nbsp; Bloqueia todos os pacotes na porta 53, efetivamente bloqueando a porta como um todo.
>
>- *`ufw deny 53/ucp`*
>>&nbsp; Bloqueia a entrada de pacotes UCP na porta 53.

</details>

#### Gerenciando Serviços
<br>

- *`ufw allow <service name>`*
>&nbsp; Permite o funcionamento do serviço através de seu nome.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw allow ssh`*
>>&nbsp; Permite o funcionamento do serviço "_**ssh**_".

</details>

- *`ufw deny <service name>`*
>&nbsp; Bloqueia o funcionamento do serviço através de seu nome.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw deny ssh`*
>>&nbsp; Bloqueia o funcionamento do serviço "_**ssh**_"

</details>

#### Gerenciando Endereços IP
<br>

- *`ufw allow from <ip address>`*
>&nbsp; Permite pacotes vindos do endereço IP especificado.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw allow from 207.46.232.182`*
>>&nbsp; Permite a entrada dos pacotes vindo do IP "207.46.232.182".

</details>

- *`ufw deny from <ip address>`*
>&nbsp; Bloqueia os pacotes vindo do endereço IP indicado.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw deny from 207.46.232.182`*
>>&nbsp; Bloqueia todos os pacotes vindo do endereço "207.46.232.182".

</details>


#### Gerencimento Avançado
<br>

- *`ufw allow from <ip address> to <destination> port <port number> proto <protocol>`*
>&nbsp; Adiciona mais restrições sobre o que será permitido, podemos adicionar apenas a porta específica, ou protocolo específico, ou então, ambos.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw allow from 207.46.232.182 to any port 41`*
>>&nbsp; Permite todo pacote vindo do endereço "207.46.232.182" para a porta 41.
>
>- *`ufw allow from 207.46.232.182 to any port 41 proto tcp`*
>>&nbsp; Permite todo pacote de protocolo TCP vindo do endereço "207.46.232.182" para a porta 41".

</details>

- *`ufw deny from <ip address> to <destination> port <port number> proto <protocol>`*
>&nbsp; Bloqueia os pacotes do protocolo designado vindos do endereço IP para a porta específica.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw deny from 207.46.232.182 to any port 33`*
>>&nbsp; Bloqueia todo pacote vindo do endereço "207.46.232.182" para a porta 33.
>
>- *`ufw deny from 207.46.232.182 to any port 33 proto ucp`*
>>&nbsp; Bloqueia todo pacote de protocolo UCP vindo do endereço "207.46.232.182" para a porta 33.

</details>

#### Apagar Regras Existentes
&nbsp; Para apagar regras criadas anteriormente, devemos saber a regra criada como um todo, ou então o número específico da regra criada (algo similar a um ID da regra).

- *`ufw delete <rule or rule number>`*
>&nbsp; Elimina a regra indicada no comando.
> <details><summary><i><b>Examples</b></i></summary>
><br>
>
>- *`ufw delete deny from 207.46.232.182`*
>>&nbsp; Apaga a regra que bloqueia todo pacote vindo do endereço "207.46.232.182".
>>
>>Supondo que esta regra tivesse como número correspondente "15", poderíamos também usar *`ufw delete 15`* para apagar tal regra.

</details>
