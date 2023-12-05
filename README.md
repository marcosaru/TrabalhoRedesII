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
<p>O Sistema Operacional escolhido foi o rock linux, devido ao seu código fonte ser o mesmo que o Red Hat. Um sistema robusto.</p>
<h2 id="keypub">4 - Chaves pública/privada</h2><br>
Responsável: Marcos.<br>
<p>Repositório padrão para guardar as chaves: ~/.ssh </p>
<p>Foram criadas três chaves ssh, uma para cada membro da equipe.</p>

<p>Configuração para desabilitar o acesso do root no SSH:</p>
<a href="https://ibb.co/q1Nk032"><img src="https://i.ibb.co/4N8Psn0/Captura-de-tela-de-2023-12-05-12-51-59.png" alt="Captura-de-tela-de-2023-12-05-12-51-59" border="0"></a><br>
<p>
Motivação para desativação do acesso root no SSH:
Existem algumas motivações para que essa ação seja realizada, já adianto que todas voltadas à segurança e hardening. Alguns motivos:

Segurança: O acesso direto ao root via SSH pode, e geralmente é, um alvo atraente para ataques de força bruta. Desativar o acesso SSH para o usuário root aumenta a segurança, pois os invasores teriam que adivinhar não apenas a senha do root, mas também o nome de usuário correto para acessar o sistema;
Erros acidentais: Limitar o acesso SSH para usuários nominais pode ajudar a prevenir erros acidentais cometidos por sysadmins. Ter que fazer login com uma conta de menor privilégio antes de usar privilégios administrativos pode fazer com que os administradores pensem duas vezes antes de realizar ações críticas;
</p>
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
<a href="https://ibb.co/sWJckGd"><img src="https://i.ibb.co/FHqcNML/https.png" alt="https" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>
<br>
<h2 id="firewall">7 - Instalação Firewall </h2><br>
<a href="https://ibb.co/Kw8dJGs"><img src="https://i.ibb.co/RyJfqS6/Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3.jpg" alt="Imagem-do-Whats-App-de-2023-10-31-s-19-58-28-c441f7d3" border="0"></a>
  <br>
<p>Responsável: Vitória <p>
<br><code><a  href="#sumario"> VOLTAR</a></code>

<h2 id= "firewallInst">7.1 - Configuração do Firewall da infra</h2><br>
Responsável: Marcos.<br>
<a href="https://ibb.co/gSGnyqK"><img src="https://i.ibb.co/rxgWk8r/firewall-Infra.png" alt="firewall-Infra" border="0"></a>
<p>As motivações para restringir o acesso a porta 22 da instância são: </p>
<p>
Restrição de Acesso: Limitar o acesso à porta 22 apenas ao seu IP significa que somente você, ou quem estiver conectado a partir do seu endereço IP específico, terá permissão para acessar o servidor via SSH. Isso reduz a superfície de ataque, tornando mais difícil para possíveis invasores tentarem ganhar acesso não autorizado.

Princípio do Privilégio Mínimo: Conceder acesso somente a partir de endereços IP específicos reduz o risco de acesso não autorizado, uma vez que apenas dispositivos confiáveis podem se conectar.

Proteção contra Ataques de Força Bruta: Limitar o acesso à porta 22 reduz a exposição a ataques de força bruta, nos quais um atacante tenta adivinhar a senha/chave privada ao tentar várias combinações. Ao restringir o acesso apenas ao seu IP, você reduz as oportunidades para esses ataques, tornando-os menos eficazes.

Monitoramento Simplificado: Ao permitir o acesso somente a partir de um conjunto específico de endereços IP, o monitoramento de atividades suspeitas torna-se mais fácil. Se há tentativas de acesso de IPs não autorizados, isso pode indicar uma possível ameaça ou atividade maliciosa.
</p>


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

<p>O SELinux (Security-Enhanced Linux) é um conjunto de extensões de segurança para o kernel Linux que fornece um sistema avançado de controle de acesso obrigatório (MAC). A implementação do SELinux oferece várias vantagens em termos de segurança, e suas motivações incluem:</p>
<p>
Controle Acesso: O SELinux permite um controle muito grande sobre os acessos dos processos aos recursos do sistema. Ele vai além das permissões tradicionais de usuário e grupo, permitindo especificar políticas de acesso para processos individuais, arquivos e recursos do sistema.

Princípio do Privilégio Mínimo: Assim como a restrição de acesso no firewall, o SELinux adere ao princípio do privilégio mínimo. Ele ajuda a limitar os privilégios concedidos a processos e usuários, reduzindo assim a superfície de ataque e minimizando o impacto de possíveis falhas de segurança.

Prevenção de Exploração de Vulnerabilidades: O SELinux pode ajudar a prevenir a exploração de vulnerabilidades de segurança ao restringir as ações que processos comprometidos podem realizar. Isso dificulta a movimentação lateral de ataques, pois os invasores teriam que contornar as políticas de segurança do SELinux.

Proteção contra Escalação de Privilégios: O SELinux desempenha um papel crucial na prevenção de escalonamento de privilégios. Mesmo se um invasor ganhar acesso inicial a um sistema, o SELinux pode limitar suas capacidades e impedir que ele aumente seus privilégios.

Reforço da Segurança em Ambientes Compartilhados: Em ambientes onde vários usuários compartilham recursos do sistema, como servidores de hospedagem web compartilhados, o SELinux pode ser essencial para isolar os processos e garantir que cada usuário tenha apenas acesso aos recursos permitidos.

Auditoria Avançada: O SELinux oferece recursos avançados de auditoria que permitem rastrear e analisar atividades suspeitas ou maliciosas no sistema. Isso é valioso para a detecção de ameaças e investigações de segurança.
Em resumo, o SELinux é motivado por um foco aprimorado na segurança, proporcionando um nível mais elevado de controle e proteção contra ameaças e explorações de segurança.

</p>
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
<a href="https://ibb.co/Smxwn64"><img src="https://i.ibb.co/FYW4whL/CIS.png" alt="CIS" border="0"></a><br>
<br>
Comprovação da implementação:<br>
<a href="https://ibb.co/p2h8bvM"><img src="https://i.ibb.co/9nZLc91/http.png" alt="http" border="0"></a>
<br>
<a href="https://ibb.co/sWJckGd"><img src="https://i.ibb.co/FHqcNML/https.png" alt="https" border="0"></a>
<br><code><a  href="#sumario"> VOLTAR</a></code>
