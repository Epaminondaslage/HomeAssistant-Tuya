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

Zigbee é um protocolo de comunicação sem fio de baixa potência, baseado no padrão IEEE 802.15.4, desenvolvido para aplicativos de Internet das Coisas (IoT) e automação residencial. É projetado para permitir a comunicação confiável e eficiente entre dispositivos que requerem baixo consumo de energia e baixa taxa de transmissão de dados.

A tecnologia Zigbee opera na banda de frequência ISM (Industrial, Scientific, and Medical) de 2,4 GHz, que também é utilizada pelo Wi-Fi e outros padrões sem fio. No entanto, o Zigbee utiliza uma arquitetura de rede em malha (mesh network), em que cada dispositivo pode atuar como um nó roteador, permitindo que os dados sejam encaminhados entre os dispositivos( dispositivos que são alimentados  por fonte de energia  que não sejam baterias), ampliando o alcance e melhorando a robustez da rede.

A principal característica do Zigbee é sua eficiência energética. Os dispositivos Zigbee são projetados para operar com baixo consumo de energia, permitindo que funcionem por longos períodos com baterias de pequena capacidade ou até mesmo com uma única bateria por anos. Essa eficiência torna o Zigbee adequado para dispositivos alimentados por bateria, como sensores, controles remotos e dispositivos de automação residencial.

O Zigbee suporta diferentes topologias de rede, incluindo a formação de redes estrela, cluster tree e malha (mesh). A topologia de malha é especialmente útil em ambientes complexos ou grandes, pois permite que os dados sejam roteados por vários caminhos, garantindo a confiabilidade da comunicação mesmo em caso de falha de um nó específico.

Em termos de segurança, o Zigbee oferece recursos robustos para proteger a integridade e a confidencialidade dos dados transmitidos. Ele utiliza criptografia AES-128 (Advanced Encryption Standard) para proteger as informações durante a transmissão, evitando assim a interceptação não autorizada.

# Plataforma Tuya

A plataforma Tuya é uma empresa chinesa que oferece uma plataforma de IoT (Internet das Coisas) que permite aos fabricantes de dispositivos criar e conectar seus produtos à nuvem e, assim, torná-los inteligentes e controláveis remotamente. Eles fornecem uma variedade de módulos de hardware e software que permitem aos fabricantes integrar facilmente funcionalidades de IoT em seus produtos. São duas as formas de conexão de equipamentos Tuya à plataforma do Home Assistant.

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

# Integração Tuya Home Assistant através da nuvem Tuya

## Criar um projeto no sites de IOT da Tuya

Acesse o site da Plataforma Tuya IoT: https://iot.tuya.com/.

Faça login na sua conta da Plataforma Tuya IoT.

No menu de navegação à esquerda, clique em "Cloud" e selecione "Development" (Desenvolvimento).

Na página de Desenvolvimento, clique em "Create Cloud Project" (Criar Projeto na Nuvem).

Na caixa de diálogo "Create Cloud Project" (Criar Projeto na Nuvem), configure os seguintes detalhes:

Project Name (Nome do Projeto): Insira um nome para o seu projeto.
Description (Descrição): Forneça uma breve descrição do seu projeto.
Industry (Indústria): Selecione a indústria relevante à qual o seu projeto pertence.
Data Center (Centro de Dados): Escolha o centro de dados apropriado para a sua localização na lista suspensa. Consulte a lista de mapeamento país/centro de dados fornecida pela Tuya para fazer a escolha correta para o seu país.
Development Method (Método de Desenvolvimento): Selecione "Smart Home" (Casa Inteligente) na lista suspensa como o seu método de desenvolvimento.
Uma vez que você tenha preenchido as informações necessárias, clique no botão "Create" (Criar) para criar o seu projeto na nuvem.

## Passos gerais para vincular dispositivos usando a conta do aplicativo Tuya

Abra o aplicativo Tuya Smart ou Smart Life em seu dispositivo móvel.

No aplicativo, acesse a seção "Me" (Eu) ou "Profile" (Perfil), onde você encontrará opções relacionadas à sua conta.

Procure por uma opção como "Link Account" (Vincular Conta) ou "Add App Account" (Adicionar Conta do Aplicativo). Essa opção permitirá vincular dispositivos à sua conta a partir de outro aplicativo.

Na seção "Add App Account" (Adicionar Conta do Aplicativo), talvez seja exibido um código QR na tela.

No Tuya IoT Platform (Plataforma Tuya IoT), vá para a guia "Devices" (Dispositivos).

Clique em "Link Tuya App Account" (Vincular Conta do Aplicativo Tuya) e selecione "Add App Account" (Adicionar Conta do Aplicativo).

Usando o aplicativo Tuya Smart ou Smart Life em seu dispositivo móvel, escaneie o código QR exibido na Plataforma Tuya IoT.

Siga as instruções no aplicativo Tuya Smart ou Smart Life para confirmar o processo de vinculação.

Após confirmar, volte para a Plataforma Tuya IoT e navegue até a guia "All Devices" (Todos os Dispositivos) para verificar se os dispositivos foram importados com sucesso.

## Passos para obter a Chave de Autorização (Authorization Key) para o seu projeto na Plataforma Tuya IoT

Faça login na Plataforma Tuya IoT (https://iot.tuya.com/).

No painel da Plataforma Tuya IoT, localize e clique no projeto que você criou anteriormente para acessar a página de Visão Geral do Projeto (Project Overview).

Uma vez na página de Visão Geral do Projeto, você deve encontrar a Chave de Autorização associada ao seu projeto. Essa chave é geralmente utilizada para configurar integrações e permitir o acesso às APIs do seu projeto na Plataforma Tuya IoT. Copie a Chave de Autorização para um local seguro ou anote-a para uso futuro.

# Configuração

Adicionar a integração Tuya à sua instância do Home Assistant pode ser feito através da interface do usuário, usando este botão "Meu":

[Tuya - Meu Botão]

O Home Assistant pode descobrir automaticamente a integração Tuya. Se uma instância for encontrada, ela será mostrada como "Descoberta". Você pode configurá-la imediatamente.

Passos de configuração manual

País
Escolha o país que você selecionou ao se registrar.

ID de Acesso à Tuya IoT (Tuya IoT Access ID)
Acesse o seu projeto na Plataforma Tuya IoT. Encontre o ID de Acesso abaixo da Chave de Autorização na guia Visão Geral do Projeto.

Segredo de Acesso à Tuya IoT (Tuya IoT Access Secret)
Acesse o seu projeto na Plataforma Tuya IoT. Encontre o Segredo de Acesso abaixo da Chave de Autorização na guia Visão Geral do Projeto.

Conta (Account)
Utilize a conta do aplicativo Tuya Smart ou Smart Life, não a conta da plataforma Tuya IoT.

Senha (Password)
Informe a senha da sua conta do aplicativo, não a senha da conta da plataforma Tuya IoT.


# Sites relacionados ao Home Assistant - Tuya
https://www.home-assistant.io/integrations/tuya/
* https://
  
# Status do Projeto

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)

