# Anotações de aula

- [--] [Trilha Fundamentar](https://github.com/andrademech/rocketseat/tree/main/Fundamentar)

# Aula 01

## Formulários

Para quê serve?
    - Capturar dados de entrada (input)
    - Interação
    - Controle

Pré requisitos:
    - Básico de HTML

Dominar:
    - Estilização
    - Validação
    - Controles customizados
    - JavaScript

Tag => form

    - Elemento que definirá um formulário
    - É um container estilo <section> <footer>

Atributos básicos 
    - action
    - method

## Fieldset

- Fieldset
    - Agrupamento de campos
    - Mesmo propósito
    - Semântico
    - Acessibilidade

- Atributos especiais
    - disabled
        - desabilita todos os elementos internos
        - não serão enviados ao submeter o formulário
    - form
        - o ID de um formulário ao qual esse fieldset pertence não precisa estar dentro do formulário
    - name
        - nome do grupo
- Legend
    - nome do agrupamento
    - primeiro elemento dentro do fieldset

## Label

- Label
    - Associar e identificar uma (ou mais) tag de entrada de dados
    - Acessibilidade
    - Você poderá clicar para mudar o foco de entrada de dados
- Atributos
    - For
        - para fazer a conexão entre este label e a tag de entrada de dados
        - é feita via ID do input
        - só funciona com elementos específicos
            - button, input (not hidden), meter, output, progress, select, textarea


## Button

- Button
    - Representa um botão
    - Usado para enviar formulários
    - É estilizado pelo user agent
- Atributos comuns
    - type
        - submit
        - reset
        - button
    - autofocus
    - disabled
    - name
    - value
    - form


## Datalist

- Datalist
    - Lista de valores como sugestão a uma tag <*input*>
    - Valores sugestivos e não obrigatórios
    - Usuário poderá selecionar um dos vlaores, ou clocar um valor diferente da sugestão

~~~javascript
<datalist id="fruitsdata">
    <option>apple</option>
    <option>banana</option>
    <option>mango</option>
    <option>orange</option>
    <option>cherry</option>
</datalist>
~~~
- Recebe como valor o id de um <*datalist*> residente no mesmo documento.

### Tipos de input suportados

- text, search, url, tel, email, date, month, week, time, datetime-local, number, range e color.

* Valores de datalist que não são compatíveis com o tipo do <*input*> não serão apresentados.

### Tipos de input não suportados (conforme especificação)

- hidden, password, checkbox, radio, file ou qualquer tipo de button

# Aula 02

## Input

-Input
    - Um dos mais usados em formulários
    - Aceita os mais diversos tipos de dados
    - Um dos mais poderosos e complexos
    - Elevado número de combinações
- Atributos
    - type
    - name
    - ID

- Atributos comuns
    - autocomplete
    - autofocus (o cursos muda automaticamente para o input)
    - disabled (desabilita o input)
    - readonly (apenas para visualizar - comum a quase todos)
    - value
    - form (linkar o input com outro formulário - comum a quase todos)
    - name
    - required (form obrigatório - comum a quase todos)
    - placeholder

## Password

- Password
    - Colocar uma senha de maneira segura
    - Esconde o que está sendo digitado no campo
    - O estilo da apresentação do campo, depende do User Agent
- Atributos
    - minlength / max length
        - O número mínimo e/ou máximo de caracteres para este campo
    - size
        - O número aceitável de caracteres que esse campo deverá conter
    - pattern
        - Espressão regular para validar o que está sendo digitado no campo
        - Altamente recomemda o uso de um padrão de segurança alta de senhas
        - Exemplo: queremos que a senha contenha caracteres hexadecimais com o limite de no mínimo 4 e no máximo 8 caracteres
            - pattern=" [0-9a-fA-F]{4,8} "
        
    - placeholder
        - Mostra um exemplo de texto a ser digitado no campo
    - readonly / disabled
        - Atrivuto booleano indicando se o campo está habilitado ou não
    - required
        - O campo será obrigatório
    - inputmode
        - poderá alterar o uso do teclado em smartphones
        - exemplo: queremos que o cliente só adicione números
            - inputmode="numeric"
    - autocomplete
        - on: permite a sugestão de: new-password ou current-password
        - off: desabilita a opção de autocomplete
        - new-password: o navegador poderá sugerir uma nova senha
    
## Email

- Email
    - Espera que o usuário digite um email
    - Irá validar se o valor digitado é um email

- Atributos 
    - placeholder
    - readonly/disabled
    - value
    - required
    - multiple
        - o campo irá receber um ou mais emails, separado por vírgulas
    - minlength / maxlength
    - size
        - o valor numérico indicando quantos caracteres esse campo deveria conter, modificando o tamanho do campo para o usuário
    - pattern
        - Uso de expressão regular para validar o campo
        - exemplo: o usuário só poderá colocar email do domínio rocketseat.com.br
            - pattern=".+@rocketseat\.com\.br"
    - list
        - o ID de uma tag <*datalist*> que está no mesmo documento 
        - o <*datalist*> irá conter uma lista de valores pré definidos a fim de sugerir ao usuário, quais valores estão disponíveis
            - os valores do <*datalist*> que não forem compatíveis com o campo, não serão apresentados como sugestão

## URL

- URL
    - Espera que o usuário digite uma URL
    - Irá validar se o valor digitado é uma URL

- Atributos 
    - placeholder
    - readonly/disabled
    - value
    - required
    - minlength / maxlength
    - size
        - o valor numérico indicando quantos caracteres esse campo deveria conter, modificando o tamanho do campo para o usuário
    - pattern
        - Uso de expressão regular para validar o campo
        - exemplo: o usuário só poderá colocar email do domínio rocketseat.com.br
            - pattern=".*\.com\.br\/.*"
    - list
        - o ID de uma tag <*datalist*> que está no mesmo documento 
        - o <*datalist*> irá conter uma lista de valores pré definidos a fim de sugerir ao usuário, quais valores estão disponíveis
            - os valores do <*datalist*> que não forem compatíveis com o campo, não serão apresentados como sugestão
    - spellcheck
        - Habilitar a verificação ortográfica para este input
            
## File

- File
    - Espera que o usuário digite uma File
    - Irá validar se o valor digitado é uma File

- Atributos 
    - value
        - contém o arquivo a ser enviado
    - accept
        - descreve que tipos de arquivos serão aceitos
        - exemplo: .doc, .docx, .pdf, audio/*, image/png, .png
    - files
        - a lista de arquivo ou arquivos
    - multiple
        - permite o envio de múltiplos arquivos
    - Envio dos arquivos
        - Para envio dos arquivos o formulário deverá utilizar o métodos POTS e o atributo enctype como "multipart/dorm-data"
## Color

- Color
    - Interface para selecionar cor
    - Color picker
- Atributos
    - value: RGB
        - Se válido, o preto será exibido
    - list
        - o ID de uma tag <*datalist*> que está no mesmo documento 
        - o <*datalist*> irá conter uma lista de valores pré definidos a fim de sugerir ao usuário, quais valores estão disponíveis
            - os valores do <*datalist*> que não forem compatíveis com o campo, não serão apresentados como sugestão
 