# WSL (Windows Subsystem for Linux)

Aqui está um passo a passo detalhado para instalar o **WSL (Windows Subsystem for Linux)** e o **Ubuntu** no seu computador com Windows:

### Passo 1: Habilitar o WSL no Windows

1. **Abrir o PowerShell como Administrador**:
   - Pressione `Win + X` e selecione "Windows PowerShell (Admin)" ou "Prompt de Comando (Admin)".
   
2. **Habilitar o WSL**:
   Execute o seguinte comando para habilitar o WSL no Windows 10 ou Windows 11:

   ```powershell
   wsl --install
   ```

   Isso irá habilitar o WSL, baixar o Ubuntu e instalar tudo automaticamente. Se você estiver utilizando uma versão mais antiga do Windows, ou se o comando não funcionar, siga os próximos passos:

### Passo 2: Habilitar o WSL manualmente (se necessário)

Se o comando acima não funcionar, siga estas etapas para instalar manualmente o WSL.

1. **Ativar o Subsistema do Windows para Linux**:
   No PowerShell (administrador), digite o seguinte comando:

   ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   ```

2. **Ativar a Plataforma de Máquina Virtual**:
   Em seguida, execute este comando para ativar a plataforma de máquina virtual necessária para o WSL 2:

   ```powershell
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
   ```

3. **Reiniciar o computador**.

### Passo 3: Instalar o Ubuntu

Após o WSL estar habilitado e o computador reiniciado:

1. **Abrir a Microsoft Store**:
   - Vá até a Microsoft Store, que pode ser encontrada no menu iniciar.

2. **Pesquisar pelo Ubuntu**:
   - Na barra de pesquisa da loja, procure por "Ubuntu".
   - Você verá várias versões do Ubuntu, como `Ubuntu 20.04 LTS`, `Ubuntu 22.04 LTS`, etc. Escolha a versão que preferir (recomendo a versão LTS, pois ela tem suporte a longo prazo).

3. **Instalar o Ubuntu**:
   - Clique na versão desejada e, em seguida, clique em "Instalar".
   
4. **Aguarde o download e instalação**.

### Passo 4: Configurar o Ubuntu

1. Após a instalação ser concluída, clique em "Iniciar" ou procure por "Ubuntu" no menu iniciar e abra o aplicativo.

2. Na primeira vez que abrir, o Ubuntu passará por um processo de configuração inicial, onde você será solicitado a criar um usuário e senha para o sistema.

### Passo 5: Atualizar o Ubuntu (recomendado)

Após a instalação, é uma boa prática atualizar o Ubuntu para garantir que todos os pacotes estejam atualizados.

1. Abra o terminal do Ubuntu e execute os seguintes comandos:

   ```bash
   sudo apt update
   sudo apt upgrade
   ```

2. Após a atualização, reinicie o Ubuntu se necessário.

### Passo 6: Verificar se o Ubuntu foi instalado corretamente

1. Para verificar se o Ubuntu foi instalado corretamente, você pode executar o comando:

   ```bash
   wsl -l -v
   ```

   Esse comando listará todas as distribuições instaladas no WSL e suas versões.

2. Você pode também rodar o seguinte comando para verificar a versão do Ubuntu:

   ```bash
   lsb_release -a
   ```

Isso deve concluir a instalação do WSL e do Ubuntu no seu Windows!
