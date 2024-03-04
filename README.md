

<h1>🚀  Criar um aplicativo Web de IA usando Python e Flask</h1>

Como trilha de apredizado do Bootcamp Back-End Python e Django, oferecido pela Mais Mulheres Tech em parceiria com WomakersCode, foi realizado o desafio Utilizando Flask para criar um web app com IA.

👉 De forma geral, o código faz o seguinte:

◻️ Lê o texto que o usuário inseriu e o idioma selecionado no formulário

◻️ Lê as variáveis ambientais que criamos anteriormente no arquivo .env

◻️ Cria o caminho necessário para chamar o serviço de Tradução, que inclui o idioma de destino (o idioma de origem é detectado automaticamente)

◻️ Cria as informações de cabeçalho, que incluem a chave para o serviço de Tradução, o local do serviço e uma ID arbitrária para a tradução

◻️ Cria o corpo da solicitação, que inclui o texto que queremos traduzir

◻️ Chama post em requests para chamar o serviço de Tradução

◻️ Recupera a resposta JSON do servidor, que inclui o texto traduzido

◻️ Recupera o texto traduzido (confira a nota a seguir)

◻️ Chama render_template para exibir a página de resposta

<h2>Tecnologias</h2>
HTML
PYTHON
AZURE
