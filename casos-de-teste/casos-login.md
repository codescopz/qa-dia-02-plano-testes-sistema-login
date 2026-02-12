## DOCUMENTO DE CASOS DE TESTE

Projeto: Sistema de Login e Recuperação de Senha
Versão: 1.1
Responsável: Natália Nascimento
Data: 12/02/2026
Ambiente de Teste:

Sistema Web

Navegador: Google Chrome 120+

Sistema Operacional: Windows 10

Base de dados: Ambiente de homologação

📊 MATRIZ DE RASTREABILIDADE
Requisito	Casos de Teste
RF01	CT-001
RF02	CT-002
RF03	CT-006
RF04	CT-007, CT-008
RF05	CT-003, CT-004, CT-005

Cobertura: ✅ 100%

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-001 – Login com dados válidos

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-001
Requisito: RF01
Tipo: Funcional
Prioridade: Alta
Severidade: Crítica
Status: Não Executado

🎯 Objetivo

Validar que o sistema permite login com credenciais válidas.

🔐 Pré-condição

Usuário previamente cadastrado e ativo na base de dados.

📥 Dados de Teste

E-mail: usuario@teste.com

Senha: 123456

🔄 Passos

Acessar a tela de login

Informar e-mail válido

Informar senha válida

Clicar em “Entrar”

✅ Resultado Esperado

Usuário deve ser autenticado com sucesso e redirecionado para a página inicial.

📎 Evidência Esperada

Print da tela inicial após login.

📌 Critério de Aprovação

Redirecionamento correto e sessão iniciada.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-002 – Login com senha incorreta

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-002
Requisito: RF02
Tipo: Negativo
Prioridade: Alta
Severidade: Alta
Status: Não Executado

🎯 Objetivo

Validar que o sistema bloqueia acesso com senha incorreta.

🔐 Pré-condição

Usuário cadastrado.

📥 Dados de Teste

E-mail: usuario@teste.com

Senha: senha_errada

🔄 Passos

Acessar a tela de login

Informar e-mail válido

Informar senha incorreta

Clicar em “Entrar”

✅ Resultado Esperado

Exibir mensagem:
"E-mail ou senha inválidos."
Usuário não deve acessar o sistema.

📎 Evidência Esperada

Print da mensagem de erro exibida.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-003 – Campo e-mail em branco

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-003
Requisito: RF05
Tipo: Validação
Prioridade: Alta
Severidade: Média
Status: Não Executado

🎯 Objetivo

Validar obrigatoriedade do campo e-mail.

🔄 Passos

Acessar tela de login

Deixar campo e-mail vazio

Informar senha válida

Clicar em “Entrar”

✅ Resultado Esperado

Sistema deve exibir mensagem informando que o campo e-mail é obrigatório.

📎 Evidência Esperada

Print da validação exibida abaixo do campo.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-004 – Campo senha em branco

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-004
Requisito: RF05
Tipo: Validação
Prioridade: Alta
Severidade: Média
Status: Não Executado

🎯 Objetivo

Validar obrigatoriedade do campo senha.

🔄 Passos

Informar e-mail válido

Deixar campo senha vazio

Clicar em “Entrar”

✅ Resultado Esperado

Sistema deve exibir mensagem informando que o campo senha é obrigatório.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-005 – E-mail em formato inválido

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-005
Requisito: RF05
Tipo: Validação
Prioridade: Alta
Severidade: Média
Status: Não Executado

🎯 Objetivo

Validar formato correto do campo e-mail.

📥 Dados de Teste

E-mail: usuario_teste
Senha: 123456

🔄 Passos

Informar e-mail inválido

Informar senha válida

Clicar em “Entrar”

✅ Resultado Esperado

Sistema deve exibir mensagem informando formato inválido.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-006 – Bloqueio após 5 tentativas inválidas

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-006
Requisito: RF03
Tipo: Segurança
Prioridade: Alta
Severidade: Crítica
Status: Não Executado

🎯 Objetivo

Garantir bloqueio da conta após múltiplas tentativas inválidas.

🔄 Passos

Informar senha incorreta

Repetir processo 5 vezes consecutivas

✅ Resultado Esperado

Conta deve ser bloqueada após a 5ª tentativa.

Mensagem:
"Conta bloqueada após múltiplas tentativas inválidas."

📎 Evidência Esperada

Print da mensagem de bloqueio.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-007 – Recuperação de senha com e-mail cadastrado

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-007
Requisito: RF04
Tipo: Funcional
Prioridade: Média
Severidade: Alta
Status: Não Executado

🎯 Objetivo

Validar envio de e-mail de recuperação.

📥 Dados de Teste

E-mail: usuario@teste.com

🔄 Passos

Clicar em “Esqueci minha senha”

Informar e-mail cadastrado

Confirmar

✅ Resultado Esperado

Sistema deve exibir mensagem de confirmação.
E-mail deve ser enviado ao usuário.

📎 Evidência Esperada

Print da mensagem + confirmação de recebimento do e-mail.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🧪 CT-008 – Recuperação com e-mail não cadastrado

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ID: CT-008
Requisito: RF04
Tipo: Negativo
Prioridade: Média
Severidade: Média
Status: Não Executado

🎯 Objetivo

Validar comportamento do sistema para e-mails inexistentes.

📥 Dados de Teste

E-mail: naoexiste@teste.com

🔄 Passos

Informar e-mail não cadastrado

Confirmar solicitação

✅ Resultado Esperado

Sistema deve informar que o e-mail não está cadastrado.
