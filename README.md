# Trabalho de Redes II
<b>UFSC 2023/2</b><br><br>
Professor <a href="https://github.com/glcamillo">Gerson Luiz Camillo</a><br><br>

Participantes: Everton, Marcos, Vitória

SUMÁRIO

1 - <a href="#MFA">Multifatorial (MFA)</a><br>
2 - <a href="#grupos-">Grupos </a><br>
2.1 - <a href="#grupo-de-gerentes">Grupo dos Gerentes</a><br>
2.1 - <a href="#grupo-cebola">Grupo Cebola </a><br>
3 - <a href="#instancia">Instância utilizada</a><br>
4 - <a href="#-chaves-públicaprivada">Chaves pública/privada</a><br>
5 - <a href="#patches">Patches</a><br>
6 - <a href="#apache2">Instalação Apache2</a><br>
6.1 - <a href="#ca">Criação da CA</a><br>
7 - <a href="#firewall">Configuração no firewall</a><br>
7.1 - <a href="#firewallInst">Configuração no firewall da instância</a><br>
8 - <a href="#restricoes">Restrições de acessos</a><br>
9 - <a href="#mac">Controle MAC</a><br>
10 - <a href="#tecnicas">Escolha das técnicas de segurança</a><br>
11 - <a href="#logs">Logs do servidor</a><br>
11.1 - <a href="#logsapache">Logs Apache</a><br>
12 - <a href="#NTP">Protocolo NTP</a><br>

<h2 id="MFA">MFA</h2><br>
<a href="https://ibb.co/xsBd5XJ"><img src="https://i.ibb.co/DbvTKz5/Captura-de-tela-de-2023-10-07-12-33-52.png" alt="Captura-de-tela-de-2023-10-07-12-33-52" border="0"></a>
<br>
<h2>Questão 2</h2><br>
Responsável: Marcos.<br>
<a  href="https://ibb.co/FDbrgbw"><img src="https://i.ibb.co/CH5ch57/Captura-de-tela-de-2023-10-06-11-38-18.png" alt="Como montar grupos" border="0" /></a>


<h2 id="grupos-" >Grupos </h2>
Responsável: Marcos.

<a href="https://ibb.co/SXfw41j"><img src="https://i.ibb.co/5WKhgz0/Captura-de-tela-de-2023-10-06-11-43-35.png" alt="Captura-de-tela-de-2023-10-06-11-43-35" border="0"></a>


<h2 id="grupo-de-gerentes">Grupo de Gerentes</h2>
Responsável: Marcos.

<a href="https://ibb.co/B4cqr5f"><img src="https://i.ibb.co/z8QG7Tm/Captura-de-tela-de-2023-11-06-08-07-51.png" alt="Captura-de-tela-de-2023-11-06-08-07-51" border="0"></a>
<a href="https://ibb.co/VM8DnTY"><img src="https://i.ibb.co/2cBPVd3/Captura-de-tela-de-2023-10-10-18-51-14.png" alt="Captura-de-tela-de-2023-10-10-18-51-14" border="0"></a>
<a href="https://ibb.co/DbkmkkG"><img src="https://i.ibb.co/xsGwGGm/Captura-de-tela-de-2023-10-10-18-51-24.png" alt="Captura-de-tela-de-2023-10-10-18-51-24" border="0"></a>


<h2 id= "#grupo-cebola">Grupo Cebola</h2>
Responsável: Marcos.

<a href="https://ibb.co/dPjqFNj"><img src="https://i.ibb.co/n76v9X6/Captura-de-tela-de-2023-11-06-08-10-02.png" alt="Captura-de-tela-de-2023-11-06-08-10-02" border="0"></a>
<a href="https://ibb.co/dWf2LgB"><img src="https://i.ibb.co/Pmrh9Qx/Captura-de-tela-de-2023-10-10-18-54-44.png" alt="Captura-de-tela-de-2023-10-10-18-54-44" border="0"></a>
<a href="https://ibb.co/L6CZC1M"><img src="https://i.ibb.co/NpLyLKX/Captura-de-tela-de-2023-10-10-18-54-56.png" alt="Captura-de-tela-de-2023-10-10-18-54-56" border="0"></a>

<h2 id="chave-publicaprivada"> Chaves pública/privada</h2><br>
Responsável: Marcos.<br>

<p>Configuração necessária para conseguir ler todas as chaves:</p>
<a href="https://ibb.co/3kpr6K8"><img src="https://i.ibb.co/wYS0Gtb/Captura-de-tela-de-2023-10-06-16-25-54.png" alt="ConfigurarChavesDiversas" border="0"></a><br>

<p>Repositório padrão para guardar as chaves: ~/.ssh </p>


<p>Atualizado o Sevidor pela VM</p>
<a href="https://ibb.co/nLvmRB2"><img src="https://i.ibb.co/fx5FQ9R/print-da-1atualizacao-19-10-23.png" alt="print-da-1atualizacao-19-10-23" border="0"></a>
Responsável: Everton

<p>Implementação e Ativação do Apache2; pela VM</p>
<a href="https://ibb.co/HVs8Xrd"><img src="https://i.ibb.co/bPZ97rJ/Captura-de-tela-2023-10-31-instalando-o-apache.png" alt="Captura-de-tela-2023-10-31-instalando-o-apache" border="0"></a>
<a href="https://ibb.co/Gcm20Gr"><img src="https://i.ibb.co/Ypgk3JV/Captura-de-tela-2023-10-31-ativando-o-apache.png" alt="Captura-de-tela-2023-10-31-ativando-o-apache" border="0"></a>
Responsavel: Everton

<h2 id= "#firewallInst"> Configuração do Firewall da infra</h2>
Responsável: Marcos.

<p>Configuração Firewall da instancia<p> 
<a href="https://ibb.co/Kw8dJGs"><img src="https://i.ibb.co/RyJfqS6/Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3.jpg" alt="Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3" border="0"></a>
  
<p>Verificação do status <p>
<a href="https://ibb.co/Y7C27rh"><img src="https://i.ibb.co/JR1nRhH/Captura-de-tela-de-2023-11-01-11-53-24.png" alt="Captura-de-tela-de-2023-11-01-11-53-24" border="0"></a>

Usuario root: Marcos

Criador da instância: Marcos

Ativação do firewall: Everton


