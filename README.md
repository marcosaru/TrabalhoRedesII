# Trabalho de Redes II
<b>UFSC 2023/2</b><br><br>
Professor <a href="https://github.com/glcamillo">Gerson Luiz Camillo</a><br><br>

Participantes: Everton, Marcos, Vitória

<a id= "sumario">SUMÁRIO</a>

1 - <a href="#MFA">Multifatorial (MFA)</a><br>
2 - <a href="#grupos-">Grupos </a><br>
2.1 - <a href="#grupo-de-gerentes">Grupo dos Gerentes</a><br>
2.2 - <a href="#grupocebola">Grupo Cebola </a><br>
3 - <a href="#instancia">Instância utilizada</a><br>
4 - <a href="#keypub">Chaves pública/privada</a><br>
5 - <a href="#patches">Patches</a><br>
6 - <a href="#apache2">Instalação Apache2</a><br>
6.1 - <a href="#ca">Criação da CA</a><br>
7 - <a href="#firewall">Configuração no firewall</a><br>
7.1 - <a href="#firewallInst">Configuração no firewall da instância</a><br>
8 - <a href="#restricoes">Restrições de acessos</a><br>
8.1 - <a href="#restricoes">Problemas</a><br>
9 - <a href="#mac">Controle MAC</a><br>
10 - <a href="#tecnicas">Escolha das técnicas de segurança</a><br>
11 - <a href="#logs">Logs do servidor</a><br>
11.1 - <a href="#logsapache">Logs Apache</a><br>
12 - <a href="#NTP">Protocolo NTP</a><br>

<a><h2 id="MFA">1 - MFA</h2><br></a>
<a href="https://ibb.co/xsBd5XJ"><img src="https://i.ibb.co/DbvTKz5/Captura-de-tela-de-2023-10-07-12-33-52.png" alt="Captura-de-tela-de-2023-10-07-12-33-52" border="0"></a>
<br>
<br><code><a  href="#sumario"> VOLTAR</a></code>
<h2 >Questão 2</h2>
Responsável: Marcos.<br>
<a  href="https://ibb.co/FDbrgbw"><img src="https://i.ibb.co/CH5ch57/Captura-de-tela-de-2023-10-06-11-38-18.png" alt="Como montar grupos" border="0" /></a>

<br><code><a  href="#sumario"> VOLTAR</a></code>
<h2 id="grupos-" >2 - Grupos </h2>
Responsável: Marcos.

<a href="https://ibb.co/SXfw41j"><img src="https://i.ibb.co/5WKhgz0/Captura-de-tela-de-2023-10-06-11-43-35.png" alt="Captura-de-tela-de-2023-10-06-11-43-35" border="0"></a>

<br><code><a  href="#sumario"> VOLTAR</a></code>
<h2 id="grupo-de-gerentes">2.1 - Grupo de Gerentes</h2>
Responsável: Marcos.

<a href="https://ibb.co/B4cqr5f"><img src="https://i.ibb.co/z8QG7Tm/Captura-de-tela-de-2023-11-06-08-07-51.png" alt="Captura-de-tela-de-2023-11-06-08-07-51" border="0"></a>
<a href="https://ibb.co/VM8DnTY"><img src="https://i.ibb.co/2cBPVd3/Captura-de-tela-de-2023-10-10-18-51-14.png" alt="Captura-de-tela-de-2023-10-10-18-51-14" border="0"></a>
<a href="https://ibb.co/DbkmkkG"><img src="https://i.ibb.co/xsGwGGm/Captura-de-tela-de-2023-10-10-18-51-24.png" alt="Captura-de-tela-de-2023-10-10-18-51-24" border="0"></a>

<br><code><a  href="#sumario"> VOLTAR</a></code>
<h2 id= "grupocebola">2.2 - Grupo Cebola</h2>
Responsável: Marcos.

<a href="https://ibb.co/dPjqFNj"><img src="https://i.ibb.co/n76v9X6/Captura-de-tela-de-2023-11-06-08-10-02.png" alt="Captura-de-tela-de-2023-11-06-08-10-02" border="0"></a>
<a href="https://ibb.co/dWf2LgB"><img src="https://i.ibb.co/Pmrh9Qx/Captura-de-tela-de-2023-10-10-18-54-44.png" alt="Captura-de-tela-de-2023-10-10-18-54-44" border="0"></a>
<a href="https://ibb.co/L6CZC1M"><img src="https://i.ibb.co/NpLyLKX/Captura-de-tela-de-2023-10-10-18-54-56.png" alt="Captura-de-tela-de-2023-10-10-18-54-56" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>
<h2 id="instancia">3 - Instancia utilizada</h2><br>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/hY6hy75/Captura-de-tela-de-2023-11-19-21-38-35.png" alt="Captura-de-tela-de-2023-11-19-21-38-35" border="0"></a>
<br>
<h2 id="keypub">4 - Chaves pública/privada</h2><br>
Responsável: Marcos.<br>
<p>Repositório padrão para guardar as chaves: ~/.ssh </p>

<code><a  href="#sumario"> VOLTAR</a></code>
<h2 id="patches">5 - Atualizado do Sevidor</h2>
<a href="https://ibb.co/nLvmRB2"><img src="https://i.ibb.co/fx5FQ9R/print-da-1atualizacao-19-10-23.png" alt="print-da-1atualizacao-19-10-23" border="0"></a><br>
Responsável: Everton
<br><code><a  href="#sumario"> VOLTAR</a></code>
<br>
<h2 id="apache2">6 - Instalação do Apache2</h2><br><code>
<a href="https://ibb.co/HVs8Xrd"><img src="https://i.ibb.co/bPZ97rJ/Captura-de-tela-2023-10-31-instalando-o-apache.png" alt="Captura-de-tela-2023-10-31-instalando-o-apache" border="0"></a>
<a href="https://ibb.co/Gcm20Gr"><img src="https://i.ibb.co/Ypgk3JV/Captura-de-tela-2023-10-31-ativando-o-apache.png" alt="Captura-de-tela-2023-10-31-ativando-o-apache" border="0"></a><br>
<br><code><a  href="#sumario"> VOLTAR</a></code>
<p>Chrony User padrão rodando</p><br>
<a href="https://ibb.co/LrrFv5Y"><img src="https://i.ibb.co/T11frLY/verificar-o-que-essa-porta-323.png" alt="verificar-o-que-essa-porta-323" border="0"></a><br>
Responsavel: Everton
<br>

<h2 id="ca">6.1 - Criação da chave privada e certificado auto assinado</h2>
<p>Material utilizado: https://access.redhat.com/documentation/pt-br/red_hat_enterprise_linux/8/html/deploying_different_types_of_servers/configuring-tls-encryption-on-an-apache-http-server_setting-apache-http-server</p><br>
<p>Material para chave: https://docs.rockylinux.org/guides/security/ssl_keys_https/#generating-ssltls-keys</p><br>
instalação do modulo SSL:<br>
<a href="https://ibb.co/MPfDgGX"><img src="https://i.ibb.co/YfX7Nyr/Captura-de-tela-de-2023-11-13-08-27-55.png" alt="Captura-de-tela-de-2023-11-13-08-27-55" border="0"></a><br>

<h2>Criação do certificado SSL</h2><br>
<a href="https://ibb.co/6YVLdxr"><img src="https://i.ibb.co/H713JsB/Captura-de-tela-de-2023-11-17-13-02-40.png" alt="Captura-de-tela-de-2023-11-17-13-02-40" border="0"></a>
<br>
<p>Configuração do apache para ler o certificado SSL</p><br>
<a href="https://ibb.co/CKrjrw9"><img src="https://i.ibb.co/m5xnxRy/Captura-de-tela-de-2023-11-17-12-53-27.png" alt="Captura-de-tela-de-2023-11-17-12-53-27" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>
<br>
<h2 id="firewall">7 - Instalação Firewall </h2><br>
<a href="https://ibb.co/Kw8dJGs"><img src="https://i.ibb.co/RyJfqS6/Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3.jpg" alt="Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3" border="0"></a>
  <br>
<p>Responsável: Vitória <p>
<br><code><a  href="#sumario"> VOLTAR</a></code>

<h2 id= "firewallInst">7.1 - Configuração do Firewall da infra</h2><br>
Responsável: Marcos.<br>
<a href="https://ibb.co/GJj2XqW"><img src="https://i.ibb.co/wL1WTfS/firewallazure.png" alt="firewallazure" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>
  
<h2 id="mac">8 - MAC (Controle de acesso mandatório - SELinux)</h2>
<p>8.1 - Problema para ativar SELinux</p><br>
<a href="https://ibb.co/4W22MjC"><img src="https://i.ibb.co/fM99tCZ/Captura-de-tela-de-2023-11-12-16-18-21.png" alt="Captura-de-tela-de-2023-11-12-16-18-21" border="0"></a><br>

<p>Tutorial seguido:</p><br>
<p>https://docs.rockylinux.org/guides/security/learning_selinux/#operating-modes</p><br>

<p>Correções aplicadas diretamente no GRUB2, foi necessário editar o arquivo de boot para o SELinux ser carregado no sistema. Após este passo o SELinux bloqueou as conexões SSH na porta 22.</p><br>
<a href="https://ibb.co/xGs2LY7"><img src="https://i.ibb.co/d6cfMt5/SELinux.png" alt="SELinux" border="0" /></a>

<br>
Material utilizado: https://docs.fedoraproject.org/en-US/quick-docs/grub2-bootloader<br>
<p>Para resolver o bloqueio da porta 22, foi utilizado o CLI da azure com o seguinte script:</p><br>

<code>az vm run-command invoke \         <br>
  --resource-group RockLinux_group \         <br>
  --name RockLinux \       <br>
  --command-id RunShellScript \         <br>
  --scripts "setenforce 0"  <br>
</code>  
  <br>
<br><code><a  href="#sumario"> VOLTAR</a></code>

<h2 id="tecnicas">9 - Técnicas </h2>
<p>Foi escolhido junto com o professor as seguintes técnicas de segurança do CIS: </p>

<p>5.6 Ensure the Default CGI Content test-cgi Script Is Removed
(Automated)<br>
Este item garante que o script de teste CGI padrão 'test-cgi' seja removido do ambiente Apache.<br>
Os scripts de teste CGI, como o test-cgi, são geralmente fornecidos como exemplos para demonstrar a funcionalidade do servidor web, mas podem representar riscos de segurança significativos se não forem removidos ou desabilitados em ambientes de produção.<br>
As principais preocupações são: revelação de informações sensíveis, potencial para exploração, ameaças contra a integridade e confidencialidade...</p><br>

<p>5.7 Ensure HTTP Request Methods Are Restricted (Automated)<br>
Este tópico visa restringir os métodos de solicitação HTTP desnecessários em um servidor Apache. O objetivo é permitir apenas os métodos GET, HEAD, POST e OPTIONS. <br>
motivação para tal restrição: PUT e DELETE são considerados de alto risco e raramente usados, ou seja, devem ser desativados.</p><br>

<p>5.8 Ensure the HTTP TRACE Method Is Disabled (Automated) (implementação bônus)<br>
Esse tópico explorado visa desabilitar o método HTTP TRACE no servidor Apache no Red Hat.<br>
O método TRACE, destinado a fins de diagnóstico, não é necessário e é suscetível a abusos, portanto, deve ser desativado por questões de segurança.</p><br>

Comprovação da pasta onde contém os scripts limpa:<br>
<a href="https://ibb.co/G5rxXJm"><img src="https://i.ibb.co/W2RxQ3C/remocao-Scripts.png" alt="remocao-Scripts" border="0" style="width: 100; height: auto;"></a><br>
<br>
Comprovação da implementação:<br>
<a href="https://ibb.co/26FjxH4"><img src="https://i.ibb.co/9vpq6S5/impl.png" alt="impl" border="0"></a>
<br>
<a href="https://ibb.co/CKrjrw9"><img src="https://i.ibb.co/m5xnxRy/Captura-de-tela-de-2023-11-17-12-53-27.png" alt="Captura-de-tela-de-2023-11-17-12-53-27" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>

<h2 id="logs">Logsss</h2>
<p>Tópico "A" </p>
