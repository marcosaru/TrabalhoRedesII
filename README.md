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

<a href="https://ibb.co/R4VQx7R"><img src="https://i.ibb.co/CsTVkWR/Captura-de-tela-de-2023-10-06-11-45-18.png" alt="Gerentes" border="0"></a>



<h2 id= "#grupo-cebola">Grupo Cebola</h2>
Responsável: Marcos.

<a href="https://ibb.co/BjcRQms"><img src="https://i.ibb.co/NptzJXY/Captura-de-tela-de-2023-10-06-11-47-12.png" alt="Cebola" border="0"></a>

<h2 id="chave-publicaprivada"> Chaves pública/privada</h2><br>
Responsável: Marcos.<br>

<p>Configuração necessária para conseguir ler todas as chaves:</p>
<a href="https://ibb.co/3kpr6K8"><img src="https://i.ibb.co/wYS0Gtb/Captura-de-tela-de-2023-10-06-16-25-54.png" alt="ConfigurarChavesDiversas" border="0"></a><br>

<p>Repositório padrão para guardar as chaves: ~/.ssh </p>
<a href="https://ibb.co/jw8V1vW"><img src="https://i.ibb.co/Ks5N3jL/Captura-de-tela-de-2023-10-06-16-22-42.png" alt="Chaves" border="0"></a><br>
Responsável: Marcos.

<h2 id= "#firewallInst"> Configuração do Firewall da infra</h2>
Responsável: Marcos.

<a href="https://ibb.co/2cRy8tR"><img src="https://i.ibb.co/xzwDmjw/Captura-de-tela-de-2023-10-06-15-13-12.png" alt="Captura-de-tela-de-2023-10-06-15-13-12" border="0"></a>

Usuario root: Marcos

Criador da instância: Marcos

Ativação do firewall: Everton
