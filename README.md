# Sistema de Ticket com Discord.py
Este bot Discord implementa um sistema de tickets usando Discord.py. Ele oferece um menu dropdown interativo para os usuários selecionarem um tópico, criarem um ticket privado e interagirem com a equipe de suporte.

## ⚙️ FUNCIONALIDADES:
- **Criação de Ticket:** Os usuários podem abrir um novo ticket selecionando uma categoria em um menu dropdown e clicando no botão "Abrir Ticket".
- **Threads Privadas:** Os tickets são criados como threads privadas, garantindo a privacidade da conversa entre o usuário e a equipe de suporte.
- **Fechamento de Ticket:** Os usuários podem fechar seus próprios tickets usando o comando /fecharticket. Moderadores com o cargo definido também podem fechar tickets.
- **Categorias Personalizáveis:** O código fornece categorias pré-definidas, mas você pode personalizá-las facilmente no código para atender às suas necessidades específicas.

## ❓ COMO USAR:

1. **Instalação:**
    - Certifique-se de ter o Python 3.7 ou superior instalado.
    - Instale as bibliotecas necessárias: discord.py e python-dotenv.
2. **Configuração:**
    - **.env:** Crie um arquivo ``.env`` na raiz do projeto e defina as seguintes variáveis de ambiente:
      - ``DISCORD_BOT_SECRET``: Token do seu bot Discord.
      - ``GUILD_ID:`` ID do seu servidor Discord.
      - ``ATENDENTE_ROLE_ID:`` ID do cargo de atendente no seu servidor.
3. **Personalização:**
      - ``Dropdown`` **class**: Ajuste as opções do menu dropdown no construtor da classe ``Dropdown`` para refletir as categorias de ticket desejadas.
      - ``CreateTicket`` **class**: Se necessário, personalize a mensagem enviada no canal do ticket.
      - **Comandos Slash**: O ID do servidor é definido nos comandos slash. Se você deseja usar o bot em vários servidores, remova o parâmetro ``guild``.
4. **Execução:**
      - Execute o arquivo ``main.py`` para iniciar o bot.
## 🪄 COMANDOS SLASH:
- ``/setup``: configura o painel de tickets no canal onde o comando é usado. Requer permissões de gerenciamento do servidor.
- ``/fecharticket``: fecha o ticket atual. Pode ser usado pelo usuário que abriu o ticket ou por um moderador.

## Observações
- Este bot usa threads privadas. Certifique-se de que seu servidor Discord tenha esse recurso ativado.
- **Não compartilhe** seu ``token`` de bot **com ninguém**.
- Este README fornece uma visão geral básica. Explore o código para entender completamente a implementação e personalizá-lo de acordo com suas necessidades.
