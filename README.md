# Criando Máquinas Virtuais no Azure

As máquinas virtuais (VMs) do Azure podem ser criadas por meio do Portal do Azure, que oferece uma interface de usuário baseada em navegador para implantar VMs que executam o Windows Server, como o `Windows Server 2022 Datacenter`. Para começar, é necessária uma assinatura do Azure, e uma conta gratuita pode ser criada caso não se tenha uma.

É importante notar que as etapas descritas no guia rápido são exclusivamente para fins educacionais e não para implantações em um ambiente de produção.

### Processo de Criação de uma VM

O processo de criação de uma VM envolve os seguintes passos:

1.  **Login no Portal do Azure.**
2.  **Criação da VM:** Pesquisar por "máquinas virtuais", selecionar "Máquinas virtuais" em Serviços, e depois clicar em **Criar** e selecionar "Máquina virtual do Azure".
3.  **Configuração da instância:** Inserir um nome para a máquina virtual (ex: `myVM`) e escolher uma imagem (ex: `Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2`). Deve-se também fornecer um nome de usuário (ex: `azureuser`) e a senha que atenda aos requisitos de complexidade (mínimo de 12 caracteres) para a conta de administrador.
4.  **Regras de porta de entrada:** Selecionar "Permitir portas selecionadas" e escolher `RDP (3389)` e `HTTP (80)` na lista suspensa para permitir o tráfego. Após a validação, a VM é criada.

### Conectando-se à VM

Após a criação, pode-se conectar-se à VM iniciando uma conexão de área de trabalho remota (RDP). Na página de visão geral da VM, seleciona-se **Conectar** > **RDP**, baixa-se o arquivo RDP e, ao abri-lo, insere-se o nome de usuário (no formato `localhost\nome de usuário`) e a senha criados para a VM.

### Testando a VM

Para ver a VM em ação, é possível instalar o servidor Web do IIS executando um comando PowerShell na VM. A página de boas-vindas do IIS pode ser visualizada colando o endereço IP da VM em um navegador.

### Limpando os Recursos

Quando os recursos não forem mais necessários, eles podem ser limpos. Na página de visão geral da VM, seleciona-se o link **Grupo de recursos** e, em seguida, **Excluir grupo de recursos** para remover a VM e todos os recursos relacionados.

Alternativamente, o Azure oferece um recurso de desligamento automático para ajudar a gerenciar custos, que pode ser configurado na seção "Operações" da VM, definindo um horário específico. É importante configurar o fuso horário corretamente, pois o UTC (Tempo Universal Coordenado) é a configuração padrão.
