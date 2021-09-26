# Para acessar servidores via JUMP/BASTION, siga o seguinte passo:

- No arquivo hosts:

> teste servidores 
>[SERVERS_teste]
>X.X.X.X

> [SERVERS_teste:vars]
> ansible_ssh_common_args='-o StrictHostKeyChecking=no -o ProxyCommand="ssh -i /home/Documents/CAMINHO_KEY_SSH -W %h:%p -q login@IP_BASTION_JUMP"'
> ansible_user=login
> ansible_pass=passwd
> ansible_become=yes
> ansible_become_method=su
> ansible_network_os=solaris

_Para acessar o servidor através do JUMP, necessário ter os pacotes python em ambos os cenários_




