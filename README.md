## Documentação do Projeto com Flask
## Pasta Projeto Flask
Criamos uma pasta na área de trabalho chamada 'projeto_com_Flask', e criamos um arquivo denominado de 'app.py'

## Instalação do UV Astral
Entramos no site do UV Astral e fomos até a parte denominada de "installation", depois copiamos o código para a instalação do UV em qualquer terminal que é 'powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex'.

## Comandos do UV 
Usamos o comando 'uv -V' para descobrir qual a versão instalada do UV, depois o 'uv init' que cria a estrutura inicial de um projeto python e 'uv venv' para criar a pasta venv(uma variável de ambiente), e depois o comando 'uv python install 3.15.0' para instalar a versão mais recente do python, depois o 'uv sync' para sincronizar todos os arquivos, depois o 'uv add Flask' para adcionar o flask e por ultimo 'uv run flask run' para rodar o arquivo python/flask.

## Código do app.py
Importamos o flask/markupsafe com o 'import', e dentro deles importamos 'Flask, request, render_template, escape'. Usamos snippets no código do app.py como o abaixo:

- app = Flask(__name__)
@app.route("/")
def ola_mundo():
    return "<p>Olá, Mundo!</p>"

E criamos uma condição para que o código python não execute sozinho e inicie com flask antes, segue abaixo:

- if __name__ == "__main__":
    app.run(debug=False, port=5000)

## Criação da pasta templates e ola.html
Criamos um bloco de código que são:
-   {% if nome %}
        <h1>Olá, {{nome}}!</h1>
    {% else %}
        <h1>Olá, Flask</h1>
    {% endif %}

Ao final para terminar é preciso do {% endif %}, pois é a forma que se acaba uma estrutura de repetição do python no  html.
