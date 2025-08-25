Clinera – Executor de Script Remoto

Clinera é um projeto simples em batch script que permite a execução de comandos diretamente de um link. Ele baixa um script remoto de uma URL fornecida e executa-o automaticamente na máquina local.

Visão Geral

O script utiliza o PowerShell para baixar um arquivo de script remoto hospedado em um repositório no GitHub. Após o download, o script é salvo temporariamente no diretório de arquivos temporários do sistema e é executado automaticamente.

Este projeto pode ser útil em situações onde você precisa executar um script sem precisar baixá-lo manualmente, além de permitir que você mantenha o script atualizado diretamente no repositório.

Como Funciona

O script baixa o arquivo de script remoto da URL fornecida.

O arquivo é armazenado em um diretório temporário no sistema (%TEMP%).

O arquivo baixado é executado imediatamente no sistema.

Requisitos

Windows (para execução de .bat).

PowerShell (para realizar a requisição HTTP).

Conexão com a internet para baixar o script remoto.

Como Usar

Clone ou Baixe o Projeto

Se você estiver clonando o repositório:

git clone https://github.com/ymuft/clinera.git


Configure o Script

Abra o arquivo clinera.bat no seu editor de texto favorito. A linha abaixo define o URL de onde o script será baixado:

set "URL=https://raw.githubusercontent.com/ymuft/clinera/refs/heads/main/comand"


Substitua esse URL por qualquer outro endereço onde seu script esteja hospedado.

Execute o Script

Após fazer o download, basta executar o arquivo clinera.bat em seu computador. O script automaticamente fará o download do script remoto e o executará.

clinera.bat

Exemplo do Código

O código abaixo mostra o funcionamento básico do script:

@echo off
title clinera

setlocal

set "URL=https://raw.githubusercontent.com/ymuft/clinera/refs/heads/main/comand"
set "TEMP_FILE=%TEMP%\script_baixado.bat"

:: Baixar o script remoto
powershell -Command "Invoke-WebRequest -Uri '%URL%' -OutFile '%TEMP_FILE%'"

:: Executar o script
call "%TEMP_FILE%"

endlocal

Explicação do Código

set "URL=...": Define a URL onde o script remoto será baixado.

set "TEMP_FILE=...": Define o caminho temporário onde o script será salvo.

powershell -Command "Invoke-WebRequest...": Usa o PowerShell para baixar o arquivo remoto da URL especificada e salvar em um arquivo temporário.

call "%TEMP_FILE%": Executa o script baixado imediatamente.

Segurança

Atenção: Sempre tenha cuidado ao executar scripts remotos. O código baixado da internet pode conter comandos maliciosos. Certifique-se de que o script hospedado na URL é confiável.

Contribuição

Sinta-se à vontade para contribuir com melhorias, relatórios de problemas ou sugestões. Se você tem um script útil para ser executado dessa maneira, adicione-o ao repositório ou envie um pull request!

Licença

Este projeto está licenciado sob a MIT License
.
