flask --app app run 
python -m venv venv
./venv/scripts/activate

GET geralmente indica que o usuário está solicitando informações. 
POST indica que o usuário precisa enviar algo e receber uma resposta.
Independentemente do verbo usado, as informações podem sempre ser retornadas para o usuário.

Digamos que criamos um aplicativo no qual o usuário deseja se registrar para uma lista de distribuição:

O usuário acessa o formulário de inscrição via GET
O usuário preenche o formulário e seleciona o botão enviar
As informações do formulário são enviadas de volta ao servidor usando POST
Uma mensagem de "êxito" é retornada ao usuário

HTML é a linguagem usada para estruturar as informações exibidas em um navegador, enquanto CSS (folhas de estilos em cascata) é usada para gerenciar o estilo e o layout.

Um modelo permite que você escreva o HTML principal (ou um modelo) e indique espaços reservados para as informações dinâmicas. Provavelmente, a sintaxe mais comum para espaço reservado é {{ }}. O Jinja, o mecanismo de modelagem para Flask, usa essa sintaxe.

A instrução de importação inclui referências a Flask, que é o núcleo de qualquer aplicativo Flask. Usaremos render_template em alguns instantes, quando quisermos retornar o HTML.

Usando @app.route, indicamos a rota que queremos criar. O caminho será /, que é a rota padrão. Indicamos que ele será usado para GET. Se uma solicitação GET chegar para /, o Flask chamará de forma automática a função declarada imediatamente abaixo do decorador, index em nosso caso. No corpo de index, indicamos que retornaremos um modelo HTML chamado index.html para o usuário.

Execute o comando a seguir a fim de definir o runtime do Flask para desenvolvimento, o que significa que o servidor será recarregado automaticamente em cada alteração
# Windows
set FLASK_ENV=development

Chave 
78b9987049bc4acb85c981fc66cd45f8
brazilsouth
text https://api.cognitive.microsofttranslator.com/
document https://ai-sarah.cognitiveservices.azure.com/

O código é comentado para descrever as etapas que estão sendo realizadas. De forma geral, o código faz o seguinte:

Lê o texto que o usuário inseriu e o idioma selecionado no formulário
Lê as variáveis ambientais que criamos anteriormente no arquivo .env
Cria o caminho necessário para chamar o serviço de Tradução, que inclui o idioma de destino (o idioma de origem é detectado automaticamente)
Cria as informações de cabeçalho, que incluem a chave para o serviço de Tradução, o local do serviço e uma ID arbitrária para a tradução
Cria o corpo da solicitação, que inclui o texto que queremos traduzir
Chama post em requests para chamar o serviço de Tradução
Recupera a resposta JSON do servidor, que inclui o texto traduzido
Recupera o texto traduzido (confira a nota a seguir)
Chama render_template para exibir a página de resposta