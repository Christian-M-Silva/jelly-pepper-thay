# REGRAS DE NEGÓCIO

### REGRA 001 - Visualização de produtos
**Descrição:** O comprador só poderá visualizar o produto se a vendedora não tiver desativado o produto
**Aplica-se a:** Cliente  
**Onde:** Tela de visualizar produtos no lado do vendedor 
**Motivo:** Permite vendedora desativar o produto se ele estiver temporariamente em falta  
**Ação esperada:** O sistema não deve exibir os produtos desativados.

### REGRA 002 - Alterar a senha com ID diferentes
**Descrição:** A cada vez, antes de enviar o e-mail contendo o link da alteração do e-mail, será gerado um id que será salvo na coluna da tabela de User. Esse id deverá fazer parte do param query da rota de alterar senha  para validar se o link de alterar senha é valido ou não.
**Aplica-se a:** Vendedora  
**Onde:** Tela de login e Tela de alterar senha
**Motivo:** Como só existe um unico usuario, precisa fazer uma proteção no link de alterar senha desse usuario
**Ação esperada:** O sistema criar diferentes ids, armazena eles no banco de dados e usa ele na geração do URL de alteração de senha.

### REGRA 003 - Criptografar senha
**Descrição:** A cada vez que salvar a senha, sempre tem que criptografa ela.
**Aplica-se a:** Vendedora  
**Onde:** Tela de alterar senha
**Motivo:** Trazer segurança nas senhas
**Ação esperada:** O sistema criptografa a senha antes de salvar ela.

### REGRA 004 - Autenticação com Token
**Descrição:** Após o back validar que as credenciais estão certas, deverá ser gerado um ``AcessToken`` (Que dura 15 min) e um ``RefreshToken`` (Que dura 3 dias). No Front ao tentar acessar as telas autenticadas (Visualizar produtos, adicionar e editar produtos) deverá ser validado se o usuario tem autenticação do Token. Se não tiver deverá ser verificado se o ``AcessToken`` é valido e não está expirado. Se o ``AcessToken`` estiver expirado deverá tentar usar o ``RefreshToken``, se ele ele também estiver expirado deverá retornar para a tela de login.
**Aplica-se a:** Vendedora  
**Onde:** Telas de Visualizar produtos, adicionar e editar produtos
**Motivo:** Evitar a necessidade de fazer vários logins
**Ação esperada:** O sistema deve manter o usuario logado se o token ainda estiver valido, do contrario o redireciona para a tela de Login.

### REGRA 005 - Modal de confirmação
**Descrição:** O modal só será de confirmação se o usuario enviar alguma função, onde os botões de sim ou não só apareceram se cada uma tiver uma confirmação
**Aplica-se a:** Sistema  
**Onde:** Componente de modal
**Motivo:** Flexibilidade no uso do componente
**Ação esperada:** O sistema deve exibi os botões sim e não quando cada um tiver uma ação passada para eles