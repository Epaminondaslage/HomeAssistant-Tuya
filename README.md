<td style="width: 20%;"><img src="https://github.com/Epaminondaslage/Automacao-industrial-e-residencial-Ecossistema-didatico/blob/main/img/Logo_CEFET-MG.png" width="20%"></td>
<p><strong>Home Assistant-Tuya </strong></p>
<p><strong>Prof Epaminondas Lage</strong></p>
<a href="http://lattes.cnpq.br/7787341723868111"> Currículo Lattes LAGE, E. S.</a> 

# Índice 
* [Introdução](#Introdução)
* [Zigbee](#Zigbee)
* [Plataforma Tuya](#Plataforma-Tuya)
* [Integração Tuya Home Assistant através da nuvem Tuya](#Integração-Tuya-Home-Assistant-através-da-nuvem-Tuya)



#  Introdução

Devido às suas características, o Zigbee é amplamente utilizado em dispositivos de automação residencial, como lâmpadas inteligentes, termostatos, sensores de movimento, fechaduras eletrônicas, entre outros. A capacidade de criar redes de dispositivos interconectados de maneira eficiente, segura e com baixo consumo de energia torna o Zigbee uma escolha popular para a construção de sistemas de casa inteligente e soluções IoT em geral.

A Integração de Zigbee no Home Assistant necessita um hardware compatível que funcione como uma ponte Zigbee para o seu sistema. Existem várias opções disponíveis, como dongles USB Zigbee, placas Zigbee embutidas em controladores específicos ou gateways Zigbee dedicados. Esses dispositivos permitem que o Home Assistant se comunique com os dispositivos Zigbee em sua casa.Entres gateway destaca-se osfabricados pela Tuya


# Zigbee

O Zigbee é um protocolo de comunicação sem fio baseado no padrão IEEE 802.15.4, projetado para redes de área pessoal de baixo consumo de energia e baixo custo. Ele opera na faixa de frequência de 2,4 GHz, utilizando modulação de espectro espalhado em frequência (DSSS) para transmissão de dados.

Uma das principais características do Zigbee é sua capacidade de formar redes em malha (mesh networks). Nesse tipo de rede, os dispositivos Zigbee se comunicam uns com os outros, criando rotas de comunicação redundantes e dinâmicas. Isso proporciona maior robustez e confiabilidade, permitindo que os dados sejam roteados de forma eficiente mesmo em ambientes com obstáculos físicos ou dispositivos distantes da fonte de comunicação.

Em termos de topologia de rede, o Zigbee adota uma estrutura de estrela estendida, onde um dispositivo central atua como coordenador da rede, enquanto os demais dispositivos são nós ou dispositivos finais. Essa estrutura permite uma fácil expansão da rede, pois novos dispositivos podem ser adicionados sem a necessidade de reconfigurar toda a rede.

O Zigbee possui três tipos principais de dispositivos: coordenador, roteador e dispositivo final. O coordenador é responsável por iniciar a rede e coordenar as operações de comunicação. Os roteadores funcionam como nós intermediários, encaminhando os dados entre dispositivos finais e o coordenador. Os dispositivos finais são os dispositivos que fornecem funcionalidades específicas, como sensores, atuadores ou dispositivos de controle.

Uma das vantagens do Zigbee é seu baixo consumo de energia. Os dispositivos Zigbee são projetados para operar por longos períodos com baterias de pequena capacidade ou até mesmo por meio de fontes de energia colhidas do ambiente, como energia solar ou vibração. Isso os torna ideais para aplicações em automação residencial, onde muitos dispositivos podem estar em operação contínua. Além disso, o Zigbee oferece recursos avançados de segurança. Ele suporta criptografia AES-128 para garantir a confidencialidade dos dados transmitidos e autenticação baseada em chaves para verificar a integridade dos dispositivos na rede. Isso ajuda a proteger contra ataques de interceptação de dados e falsificação de dispositivos.

A integração do Zigbee com a plataforma Tuya permite que os usuários controlem e gerenciem seus dispositivos Zigbee por meio do aplicativo Tuya. A plataforma Tuya oferece uma ampla gama de recursos para personalizar e automatizar a operação dos dispositivos. Os usuários podem criar cenas, definir programações, receber notificações e até mesmo controlar os dispositivos por meio de assistentes de voz compatíveis, como Amazon Alexa e Google Assistant.

No processo de integração, é importante garantir a compatibilidade dos dispositivos Zigbee com a plataforma Tuya. Alguns dispositivos Zigbee podem exigir um gateway Zigbee compatível com a plataforma Tuya para permitir a conexão com o aplicativo. O gateway atua como um ponto central de comunicação entre os dispositivos Zigbee e o aplicativo Tuya.

# Plataforma Tuya

A plataforma Tuya é uma empresa chinesa que oferece uma plataforma de IoT (Internet das Coisas) que permite aos fabricantes de dispositivos criar e conectar seus produtos à nuvem e, assim, torná-los inteligentes e controláveis remotamente. Eles fornecem uma variedade de módulos de hardware e software que permitem aos fabricantes integrar facilmente funcionalidades de IoT em seus produtos. 

A integração do Tuya com dispositivos Zigbee permite uma automação residencial eficiente e flexível. Ao combinar o protocolo Zigbee com a plataforma Tuya, os usuários podem desfrutar de uma ampla gama de recursos e funcionalidades para tornar suas casas mais inteligentes e personalizadas.

Com a integração do Tuya, os usuários podem controlar remotamente suas luzes, termostatos, sensores e outros dispositivos Zigbee por meio do aplicativo Tuya. Além disso, eles têm a capacidade de criar automações personalizadas, definir cenas e programar rotinas para atender às suas necessidades específicas.

São duas as formas de conexão de equipamentos Tuya à plataforma do Home Assistant.

1-Integração Tuya Home Assistant através da nuvem Tuya
  
A integração permite o acesso remoto aos dispositivos Tuya conectados ao Home Assistant. Isso significa que você pode controlar os dispositivos de qualquer lugar, desde que tenha uma conexão à internet. O Home Assistant oferece recursos avançados de controle para dispositivos Tuya, permitindo a criação de automações complexas e personalizadas. Com o Home Assistant, é possível definir regras específicas para acionar os dispositivos com base em diferentes condições, como horários, eventos, sensores ou outras variáveis.

Através do Home Assistant, os dispositivos Tuya podem ser integrados a outros dispositivos e sistemas inteligentes. Isso cria um ecossistema de automação mais completo, permitindo interações entre dispositivos de diferentes marcas e protocolos.

2-Integração local Tuya com o Home Assistant

A integração do Home Assistant com dispositivos Tuya é possível devido a um componente chamado "Tuya Local". Essa integração é interessante porque muitos dispositivos Tuya dependem tradicionalmente de uma conexão com os servidores da Tuya na nuvem para funcionar. Isso significa que, sem a conexão à internet ou em caso de falha nos servidores, os dispositivos podem se tornar inoperáveis.

O componente Tuya Local explora a capacidade oculta de alguns dispositivos Tuya para serem controlados localmente, ou seja, diretamente pela rede local, sem depender dos servidores externos da Tuya. Essa funcionalidade local normalmente não é divulgada ou oficialmente documentada pela Tuya, mas foi descoberta por meio de engenharia reversa por membros da comunidade do Home Assistant. Maiores informações no git https://github.com/make-all/tuya-local

Para utilizar a integração Tuya Local no Home Assistant, você precisará dos seguintes requisitos:
<ul>
<li>Dispositivos Tuya compatíveis: Nem todos os dispositivos Tuya suportam controle local. É importante verificar se o dispositivo  é compatível antes de prosseguir.</li>
<li>Gateway Tuya/Smart Life desbloqueado: Para permitir o controle local, é necessário desbloquear o gateway Tuya/Smart Life e, em alguns casos, instalar firmware personalizado que suporte o controle local. Isso requer conhecimentos avançados em hacking de hardware e pode anular a garantia do dispositivo, portanto, tenha cuidado.</li>
<li>Componente Tuya Local no Home Assistant: O Home Assistant possui o componente Tuya Local, que permite a integração dos dispositivos Tuya compatíveis, controlando-os diretamente pela rede local.</li>
</ul>

Por meio dessa integração, você pode conectar os dispositivos Tuya ao Home Assistant, obtendo controle total sobre eles, sem depender dos servidores da Tuya na nuvem. Isso pode trazer mais confiabilidade e privacidade à sua automação residencial, já que os comandos e dados permanecem dentro de sua rede local, sem a necessidade de compartilhá-los com servidores externos.

# Gateway Tuya

O gateway Tuya é um dispositivo central que atua como um hub de comunicação para os dispositivos inteligentes conectados à plataforma Tuya. Ele permite a interconexão e o controle dos dispositivos Tuya em um único ponto central, oferecendo uma maneira conveniente de gerenciar e automatizar sua casa inteligente.

O gateway Tuya é responsável por fornecer uma interface de comunicação entre os dispositivos Tuya e o aplicativo móvel Tuya ou outros sistemas de automação residencial compatíveis. Ele funciona como um ponto central para o controle e o gerenciamento dos dispositivos, permitindo que você os controle remotamente, crie automações personalizadas e monitore seu status.

Principais recursos do gateway Tuya:

1. Conectividade: O gateway Tuya utiliza tecnologias como Wi-Fi, Zigbee ou Bluetooth para se comunicar com os dispositivos inteligentes conectados. Ele atua como uma ponte entre os dispositivos e o aplicativo Tuya, permitindo o controle remoto e a troca de informações entre eles.

2. Controle Centralizado: Com o gateway Tuya, você pode controlar todos os dispositivos Tuya conectados a ele por meio do aplicativo Tuya ou de outros sistemas de automação residencial compatíveis. Isso significa que você pode ligar e desligar as luzes, ajustar a temperatura do termostato, controlar as tomadas, monitorar câmeras de segurança e muito mais, tudo de um único local.

3. Integração com Automação: O gateway Tuya permite a criação de automações personalizadas para seus dispositivos. Por exemplo, você pode programar as luzes para ligarem automaticamente quando você chegar em casa, configurar um cronograma para ligar e desligar os dispositivos em determinados horários ou criar regras baseadas em eventos específicos, como o acionamento de um sensor de movimento.

# Integração Tuya Home Assistant através da nuvem Tuya

## Criar um projeto no sites de IOT da Tuya

<ul>
<li>Acesse o site da Plataforma Tuya IoT: https://iot.tuya.com/. Faça login na sua conta da Plataforma Tuya IoT.</li>

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig01.png" width="50%" /></td></tr><tr>
<td style="text-align: center;">Abra o site: iot.tuya.com e registre-se.</td></tr></body></table>

<li>No menu de navegação à esquerda, clique em "Cloud" e selecione "Development" (Desenvolvimento). Na página de Desenvolvimento, clique em "Create Cloud Project" (Criar Projeto na Nuvem)</li>

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig02.png" width="50%" /></td></tr><tr>
<td style="text-align: center;">Clicar em "Cloud"</td></tr></body></table>

<li>Na caixa de diálogo "Create Cloud Project" (Criar Projeto na Nuvem), configure os seguintes detalhes:</li>

  Project Name (Nome do Projeto): Insira um nome para o seu projeto.
  Description (Descrição): Forneça uma breve descrição do seu projeto.
  Industry (Indústria): Selecione a indústria relevante à qual o seu projeto pertence.
  Data Center (Centro de Dados): Escolha o centro de dados apropriado para a sua localização na lista suspensa. Consulte a lista de    mapeamento país/centro de dados fornecida pela Tuya para fazer a escolha correta para o seu país.
  Development Method (Método de Desenvolvimento): Selecione "Smart Home" (Casa Inteligente) na lista suspensa como o seu método de     desenvolvimento.
  Uma vez que você tenha preenchido as informações necessárias, clique no botão "Create" (Criar) para criar o seu projeto na nuvem.
</ul>
<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig03.png" width="50%" /></td></tr><tr>
<td style="text-align: center;"> Preencha os campos. Escolha o datacenter Westerm America.</td></tr></body></table>
 
## Passos gerais para vincular dispositivos usando a conta do aplicativo Tuya

<ul>
<li>Abra o aplicativo Tuya Smart ou Smart Life em seu dispositivo móvel.</li>

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig04.png" width="30%" /></td></tr><tr>
<td style="text-align: center;">Caso ja tenha instalado o App Tuya em seu cel abra-o.</td></tr></body></table>

<li>No aplicativo, acesse a seção "Min" (Eu) ou "Profile" (Perfil), onde você encontrará opções relacionadas à sua conta. Procure por uma opção como "Link Account" (Vincular Conta) ou "Add App Account" (Adicionar Conta do Aplicativo). Essa opção permitirá vincular dispositivos à sua conta a partir de outro aplicativo.</li>

<li>Na seção "Add App Account" (Adicionar Conta do Aplicativo), será exibido um código QR na tela.</li>

<li>No Tuya IoT Platform (Plataforma Tuya IoT), vá para a guia "Devices" (Dispositivos).</li>

<li>Clique em "Link Tuya App Account" (Vincular Conta do Aplicativo Tuya) e selecione "Add App Account" (Adicionar Conta do Aplicativo).</li>

<li>Usando o aplicativo Tuya Smart ou Smart Life em seu dispositivo móvel, escaneie o código QR exibido na Plataforma Tuya IoT. Siga as instruções no aplicativo Tuya Smart ou Smart Life para confirmar o processo de vinculação.</li>

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig05.png" width="50%" /></td></tr><tr>
<td style="text-align: center;">Escaneie o QRcode com o App Tuya.</td></tr></body></table>

<li>Após confirmar, volte para a Plataforma Tuya IoT e navegue até a guia "All Devices" (Todos os Dispositivos) para verificar se os dispositivos foram importados com sucesso.</li>
</ul>

## Passos para obter a Chave de Autorização (Authorization Key) para o seu projeto na Plataforma Tuya IoT

<ul>
<li>Faça login na Plataforma Tuya IoT (https://iot.tuya.com/).</li>
<li>No painel da Plataforma Tuya IoT, localize e clique no projeto que você criou anteriormente para acessar a página de Visão Geral do Projeto (Project Overview).</li>
<li>Uma vez na página de Visão Geral do Projeto, você deve encontrar a Chave de Autorização associada ao seu projeto. Essa chave é geralmente utilizada para configurar integrações e permitir o acesso às APIs do seu projeto na Plataforma Tuya IoT. Copie a Chave de Autorização para um local seguro ou anote-a para uso futuro.</li>
</ul>

## Configuração

Adicionar a integração Tuya à sua instância do Home Assistant pode ser feito através da interface do usuário, usando este botão "Meu":
  O Home Assistant pode descobrir automaticamente a integração Tuya. Se uma instância for encontrada, ela será mostrada como "Descoberta". 

Passos de configuração manual
<ul>
  <li>País : Escolha o país que você selecionou ao se registrar.</li>
  <li>ID de Acesso à Tuya IoT (Tuya IoT Access ID) : Acesse o seu projeto na Plataforma Tuya IoT. Encontre o ID de Acesso abaixo da Chave de Autorização na guia Visão Geral do Projeto.</li>
   <li>Segredo de Acesso à Tuya IoT (Tuya IoT Access Secret): Acesse o seu projeto na Plataforma Tuya IoT. Encontre o Segredo de Acesso abaixo da Chave de Autorização na guia Visão Geral do Projeto.</li>
  <li>Conta (Account): Utilize a conta do aplicativo Tuya Smart ou Smart Life, não a conta da plataforma Tuya IoT.</li>
   <li>Senha (Password): Informe a senha da sua conta do aplicativo, não a senha da conta da plataforma Tuya IoT.</li>
</ul>

Segundo os passos todos os dispositivos cadastrados na nuvem da Tuya irão aparecer na Integração Tuya do Home Assistant.

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig07.png" width="50%" /></td></tr><tr>
<td style="text-align: center;">Menu Integração Tuya.</td></tr></body></table>

<table border="0"><body><tr>
<td style="width: 50%;"><img src="/img/fig06.png" width="50%" /></td></tr><tr>
<td style="text-align: center;">Abra a aba "Dispositivos".</td></tr></body></table>

# Sites relacionados ao Home Assistant - Tuya

https://www.home-assistant.io/integrations/tuya/
https://github.com/tuya/tuya-home-assistant
https://github.com/tuya/tuya-home-assistant/blob/main/docs/regions_dataCenters.md
# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

