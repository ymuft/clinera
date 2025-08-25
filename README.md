Clinera – Executor de Script Remoto

Clinera é um projeto simples em batch script que permite a execução de comandos diretamente de um link. Ele baixa um script remoto de uma URL fornecida e executa-o automaticamente na máquina local.

Visão Geral

O script utiliza o PowerShell para baixar um arquivo de script remoto hospedado em um repositório no GitHub. Após o download, o script é salvo temporariamente no diretório de arquivos temporários do sistema e é executado automaticamente.

Este projeto pode ser útil em situações onde você precisa executar um script sem precisar baixá-lo manualmente, além de permitir que você mantenha o script atualizado diretamente no repositório.

Como Funciona

O script baixa o arquivo de script remoto da URL fornecida.

O arquivo é armazenado em um diretório temporário no sistema (%TEMP%).

O arquivo baixado é executado imediatamente no sistema.



Configure o Script

Execute o Script

Após fazer o download, basta executar o arquivo clinera.bat em seu computador. O script automaticamente fará o download do script remoto e o executará.

clinera.bat

Sinta-se à vontade para contribuir com melhorias, relatórios de problemas ou sugestões. Se você tem um script útil para ser executado dessa maneira, adicione-o ao repositório ou envie um pull request!

