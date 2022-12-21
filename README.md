# projeto-safado-de-conclusao-do-modulo-Magento2

OBS: considerando que você ja tenha o Docker desktop e o majento2 instalados e funcionando na sua maquina faça os seguintes passos.

1.copie a pasta DigitalCollege para dentro do seu diretorio Y:\home\{author}\docker-magento2\src\app\code

2.rode o seguinte comando no terminal do linux:

<code>cd docker-magento2</code>

<code>bin/start</code>

Após verificar que todos os container foram inicializados corretamente e estao todos rodando.

depois faça esse comando

<code>bin/shell</code>


desabilite esse modulos com o comando

<code>bin/magento module:enable Magento_InventoryElasticsearch</code>


e então habilite o novo modulo criado com esse comando

<code>bin/magento module:enable DigitalCollege_Dev</code>

rode tambem os comandos para compilar e atualizar os modulos

<code>bin/magento setup:di:compile</code>

<code>bin/magento setup:upgrade</code>

e rode tambem esse comando para limpar e atualizar a memoria cache

<code>bin/magento cache:clean && bin/magento cache:flush</code>

agora vá ao seu navegador de preferência e acesse após ter cadastrado aguns produtos no admin do magento

<code>http://localhost/rest/V1/custom/products</code>

e pra acessar apenas um produto dentre todos por uma id acesse
<code>http://localhost/rest/V1/custom/products/{ID DO PRODUTO DESEJADO}</code>




