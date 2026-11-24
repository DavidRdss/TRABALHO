# Barbearia - atividade

A página foi criada em `barbearia/index.html`, com os estilos em `barbearia/style.css`.

## Fluxo de acesso

1. A pessoa abre `login/login.html`.
2. O formulário exige o preenchimento dos campos de identificação e senha.
3. Ao enviar, o JavaScript grava somente a marcação `barbearia-demo-access=1` em `sessionStorage`.
4. A pessoa é direcionada para `barbearia/index.html`.
5. A página da barbearia verifica essa marcação. Sem ela, redireciona de volta ao login.
6. O botão **Sair** remove a marcação e retorna ao login.

## Credenciais e tokens

Este fluxo é apenas demonstrativo e roda inteiramente no navegador. Os campos são validados quanto ao preenchimento, mas não existe consulta a uma API, banco de dados ou servidor de autenticação. A senha não é armazenada, enviada nem transformada em token. O valor em `sessionStorage` é apenas uma sinalização de navegação, pode ser alterado pelo próprio usuário e não protege dados reais.

Para uso em produção, a autenticação deve ser implementada no backend, com HTTPS, armazenamento seguro de senhas (hash com salt), sessões ou tokens emitidos e validados pelo servidor, além de controles de autorização.
