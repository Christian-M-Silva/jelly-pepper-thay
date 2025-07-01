# Fluxo de telas

## Componentes
- Input com label sem validação nele 
- Botão 
- Modal com titulo opcional e com descrição e com 2 botões opcionais, sim e não
- Toast

## Tela de login
- Background
- Campo de e-mail (Componente de input)
  - Obrigatorio e tem que ser e-mail
  - Mensagem de erro obrigatorio: Esse campo é obrigatorio
  - Mensagem de erro e-mail: Esse dado não é um e-mail
- Campo de senha (Componente de input)
  - Obrigatorio
  - Mensagem de erro obrigatorio: Esse campo é obrigatorio
- Modal informando para verificar e-mail (Não mencionar o nome do e-mail) (Componente de Modal)
- Link para alterar senha (Que chama o modal de verificar e-mail)
- Botão de login que pode chamar (Componente de Botão):
  - Chama a tela de Listar produtos ADM
  - Se der erro toast informando a mensagem de erro (Componente de toast)

## Tela de alterar senha
- Background mesmo da tela de login
- Campo de senha nova
  - Obrigatorio e com no minimo 7 caracteres
  - Mensagem de erro obrigatorio: Esse campo é obrigatorio
  - Mensagem de erro min caracter: No minimo 7 caracteres
- Campo de confirmar senha nova
  - Tem que ser o mesmo valor do campo de senha nova 
- Botão de enviar senha nova (Que redireciona para tela de login)
  - Só acionado quando todas as regras dos inputs respeitado

## Tela de Listar produtos ADM
- Icone de loading, para carregar os produtos
- Algum componente que permita visualizar os produtos, com seu nome, valor e foto e que possa selecionado, sendo que essa seleção tem que ser possivel em massa e permitir inverter o status do is_active e que ao selecionar ou clicar eu possa alterar o valor 
- Botão de cadastrar produto (Ao ser clicado leva para a tela de add produtos) (Componente de botão)
- Botão de excluir produto (Ao ser clicado abre modal de confirmação) (Componente de botão)
- Modal de confirmação (Componente de Modal) (Ambas opções fecha o modal)

## Tela de Add produtos ADM
## Tela de Editar produtos ADM
## Tela de listar produtos para compra
## Tela de carrinho
