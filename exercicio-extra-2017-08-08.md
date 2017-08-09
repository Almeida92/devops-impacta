# Apache Http server 2.3 - 2.4:
## Novos módulos
 - mod_proxy_fcgi
 - mod_proxy_scgi
 - mod_proxy_express
 - mod_remoteip

# Apache Http server 2.1 - 2.2
## Melhorias nos módulos
  - mod_authnz_ldap
  - mod_info
  
  
# NGINX

Mudanças com nginx 1.13.4 08 de agosto de 2017

    *) Característica: o ngx_http_mirror_module.

    *) Bugfix: as conexões do cliente podem ser descartadas durante a configuração
       Teste ao usar o parâmetro "reuseport" do "listen"
       Diretiva no Linux.

    *) Bugfix: o corpo do pedido pode não estar disponível nas subsequências se fosse
       Salvo em um arquivo e o proxy foi usado.

    *) Bugfix: o cache de limpeza com base no parâmetro "max_size" não funcionou
       No Windows.

    *) Bugfix: qualquer alocação de memória compartilhada exigiu 4096 bytes no Windows.

    *) Bugfix: o trabalhador nginx pode ser encerrado de forma anormal ao usar o
       Diretiva de "zona" dentro do bloco "upstream" no Windows.


Mudanças com nginx 1.13.3 11 de julho de 2017

    *) Segurança: uma solicitação especialmente criada pode resultar em um número inteiro
       Transbordamento e processamento incorreto de intervalos no filtro de alcance,
       Potencialmente resultando em vazamento de informação sensível (CVE-2017-7529).


Alterações com nginx 1.13.2 27 Jun 2017

    *) Mudança: nginx agora retorna 200 em vez de 416 quando um intervalo começa
       Com 0 é solicitado a partir de um arquivo vazio.

    *) Característica: a diretiva "add_trailer".
       Obrigado a Piotr Sikora.

    *) Bugfix: nginx não pôde ser criado em Cygwin e NetBSD; O erro ocorreu
       Apareceu em 1.13.0.

    *) Bugfix: nginx não pôde ser criado em MSYS2 / MinGW de 64 bits.
       Obrigado a Orgad Shaneh.

    *) Bugfix: uma falha de segmentação pode ocorrer em um processo de trabalho quando
       Usando o SSI com muitas inclusões e proxy_pass com variáveis.

    *) Bugfix: no ngx_http_v2_module.
       Obrigado a Piotr Sikora.


Alterações com nginx 1.13.1 30 de maio de 2017

    *) Recurso: agora um nome de host pode ser usado como o "set_real_ip_from"
       Parâmetro diretivo.

    *) Característica: sintaxe vim realçando melhorias de scripts.

    *) Característica: a diretiva "worker_cpu_affinity" agora funciona na DragonFly
       BSD.
       Obrigado a Sepherosa Ziehau.

    *) Bugfix: a renegociação de SSL nas conexões do backend não funcionou quando
       Usando OpenSSL antes de 1.1.0.

    *) Solução alternativa: o nginx não pôde ser criado com o Oracle Developer Studio
       12.5.

    *) Solução alternativa: agora o gerenciador de cache ignora as entradas de cache longas bloqueadas quando
       Limpeza de cache com base no parâmetro "max_size".

    *) Bugfix: as conexões SSL do cliente foram imediatamente encerradas se diferidas
       Aceitar e o parâmetro "proxy_protocol" da diretiva "ouvir"
       foram usados.

    *) Bugfix: na diretiva "proxy_cache_background_update".

    *) Solução alternativa: agora a diretiva "tcp_nodelay" define o TCP_NODELAY
       Opção antes de um aperto de mão SSL.
