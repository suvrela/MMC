# Relatório Sobre Formatação de computadores 
## Aula 06
### **Estudante:** Raylan Avilar  26/10/2023

Nas últimas aulas vimos sobre formatação de computadores e instalação de sistemas operacionais. Em primeiro momento, aprendemos como instalar o sistema operacional Linux (ubuntu). Por causa de alguns problemas, tivemos que retirar do computador o Windows e deixar somente o Ubuntu. Na aula Seguinte, Fizemos a instalação do Windows e deixando somente ele. No decorrer dessas aulas vimos sobre principalmente a respeito de partição de disco, partição lógica, primária e secundária. Aprendemos a respeito também da alteração da ordem da inicialização de sistema dual boot. vimos que só consiguimos trocar a ordem se formos pelo terminal do Linux. Em seguida colocarei o passo a passo de como configurar. 

Antes de configurarmos, precisamos ir na BIOS do computador para mudar a configuração. 
Para entrar na BIOS, fique apertando a tecla f2 quando ligar o PC. Depois vá em System Configuration - SATA Operation - 

Mudando a ordem de boot no Ubuntu (ou similares) com GRUB 2:

1. Verifique no prompt do boot, qual a ordem do S.O. que você quer.
(Por exemplo: a primeira linha no prompt tem a ordem zero, a segunda 1 e assim por diante. Suponha que o S.O. selecionado esteja na ordem 5 (cinco).)

2. Abra o arquivo, em /etc/default/grub:
 $ sudo gedit /etc/default/grub
3. Procure a linha: GRUB_DEFAULT=0
    E mude para:
    GRUB_DEFAULT= mude para a ordem que se encontra o windows no seu computador
    Salve e feche o arquivo.
4. Depois, rode o comando:
    sudo update-grub
    No próximo boot, a quinta linha do prompt será executada por padrão, abrindo o S.O. selecionado.



**REFERÊNCIAS**

Alterar a ordem de boot [RESOLVIDO]. Disponível em: <https://www.vivaolinux.com.br/topico/vivaolinux/Alterar-a-ordem-de-boot>. Acesso em: 27 out. 2023.

