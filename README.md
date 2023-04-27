# Configuration_Zabbix_5.0.2

Altere a senha, idioma e o tema se preferir.
![image](https://user-images.githubusercontent.com/94009104/234947193-ba1234e9-8aec-4b6d-b915-35e224dbdf8a.png)

Vamos Adicionar o boot do telegram (Crie o seu boot no telegram, adicione ele ao grupo) tenha as informações do token e o ID do grupo em mãos.

![image](https://user-images.githubusercontent.com/94009104/234948413-3fad5319-f94e-406a-92df-f50d9530a61b.png)

Adicione em ParseMode= HTML e adicione o token
![image](https://user-images.githubusercontent.com/94009104/234949059-7525e342-801b-4e51-96ed-e18d16e08ebd.png)

Vamos adicionar o ID do grupo
![image](https://user-images.githubusercontent.com/94009104/234949395-e12dbd90-4aad-42d3-a373-7e5c3a74329f.png)
![image](https://user-images.githubusercontent.com/94009104/234949485-15cf3887-3b19-4fa4-bb28-8c3853fc5f7c.png)
Adicione o ID do grupo do telegram ele sempre começa com (-)
![image](https://user-images.githubusercontent.com/94009104/234949713-2df0c595-601b-48d4-b3a0-7e3ec41fb63e.png)
Vamos criar a ação para enviar as mensagens via telegram
![image](https://user-images.githubusercontent.com/94009104/234949978-553e0bfb-0ed7-49ca-8d2c-bbaded1828dc.png)
![image](https://user-images.githubusercontent.com/94009104/234950045-1e87b7c7-712c-4b66-bec7-e6c7708ccf75.png)
![image](https://user-images.githubusercontent.com/94009104/234950125-4d41fa83-2250-4ea9-958c-d8b320733c2e.png)

Em Operações adicione:

Assunto

    ❌ Problema: <b>{HOST.NAME}</b>
Mensagem
    
    {EVENT.NAME}
    <b>{ITEM.NAME1}</b> <i>{ITEM.VALUE1}</i>
 
    Tempo do evento: {EVENT.AGE} 
    <a href="{HOST.IP}">{HOST.IP}</a>
    <i>{EVENT.SEVERITY}</i>
![image](https://user-images.githubusercontent.com/94009104/234950587-4831ff0c-36d7-44b4-a691-52ca2e6ad6a5.png)

Em Operações de recuperação, adicione:

Assunto
    
    ✅ Resolvido: <b>{HOST.NAME}</b>
Mensagem
    
    {EVENT.NAME}
    <b>{ITEM.NAME1}</b> <i>{ITEM.VALUE1}</i>
 
    Tempo do evento: {EVENT.AGE} 
    <a href="{HOST.IP}">{HOST.IP}</a>
    <i>{EVENT.SEVERITY}</i>
    ID's: {ITEM.ID}/{EVENT.ID}
![image](https://user-images.githubusercontent.com/94009104/234950984-fbbc959a-7ba2-41f5-955d-b0d1a66fe9da.png)

Em Operações de atualização, adicione:

Assunto

    Problema atualizado: {EVENT.NAME}
Mensagem

    {USER.FULLNAME} {EVENT.UPDATE.ACTION} problema em {EVENT.UPDATE.DATE} {EVENT.UPDATE.TIME}.
    {EVENT.UPDATE.MESSAGE}
    O status atual do problema é {EVENT.STATUS}, reconhecido: {EVENT.ACK.STATUS}.
![image](https://user-images.githubusercontent.com/94009104/234951355-90f844e9-5c5e-4f23-9f0a-53a118162691.png)


Nos Links Abaixo terá alguns templates disponíveis:

https://github.com/gabrielteixeiranetwork?tab=repositories

