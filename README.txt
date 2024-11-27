Sistema de Controle de Estoque
Um sistema de controle de estoque desenvolvido em PHP com suporte a SQLite, apresentando funcionalidades como entradas, saídas, e exibição do estoque atual com filtros e paginação.

Funcionalidades
Cadastro de produtos: Adição de novos produtos ao estoque.
Entradas e saídas: Registro de movimentações para controle detalhado.
Consulta com filtros: Busca de produtos por código ou localização.
Estoque atual: Exibição do saldo de estoque atualizado.
Paginação: Navegação fácil entre registros.
Controle de acesso: Níveis de permissão para usuários.
Tecnologias Utilizadas
Frontend: HTML5, CSS3, JavaScript.
Backend: PHP.
Banco de Dados: SQLite.
Gerenciamento de Sessões: PHP Sessions.

Instalação e Uso
Clone este repositório:
git clone https://github.com/AtisPolac/sistema-estoque.git
cd sistema-estoque

Configure o banco de dados:
Certifique-se de que o arquivo estoque.db existe na pasta raiz.
Caso o arquivo não esteja presente, crie manualmente usando o script SQL disponível no projeto.

Configuração de ambiente:
Configure o servidor local (ex.: XAMPP, WAMP, ou PHP embutido).
Inicie o servidor com:

php -S localhost:8000

Acesse o sistema:
Abra o navegador e acesse: http://localhost:8000.

Configurações SMTP
Para que o envio de e-mails de confirmação funcione corretamente, é necessário configurar as credenciais do servidor SMTP. Essas configurações estão localizadas no arquivos:

cadastro.php, a partir da linha 157,
login.php, a partir da linha 151
e esqueci_senha.php, a partir da linha 153

Alterações Necessárias
Configure os seguintes parâmetros com as informações do seu provedor de e-mail:
// Configurações do servidor SMTP
$mail->Host       = 'seu-servidor-smtp';
$mail->SMTPAuth   = true;
$mail->Username   = 'seu-usuario-smtp';
$mail->Password   = 'sua-senha-smtp';
$mail->SMTPSecure = 'ssl'; // ou 'tls', dependendo do provedor
$mail->Port       = 465; // ou 587, dependendo do provedor

// Configurações do e-mail
$mail->setFrom('seu-email@dominio.com', 'Nome que aparecerá no remetente');
$mail->addAddress($email); // Não altere esta linha

Exemplo de Configuração com Gmail
Se você deseja usar o Gmail, as configurações podem ser algo como:
$mail->Host       = 'smtp.gmail.com';
$mail->Username   = 'seu-email@gmail.com';
$mail->Password   = 'sua-senha';
$mail->SMTPSecure = 'tls';
$mail->Port       = 587;
$mail->setFrom('seu-email@gmail.com', 'Nome do Remetente');

Como Contribuir
Faça um fork do projeto.

Crie um branch para sua feature:
git checkout -b minha-nova-feature

Faça suas alterações e realize o commit:
git commit -m "Adiciona nova feature"

Envie para o repositório remoto:
git push origin minha-nova-feature

Abra um pull request no repositório principal.

Licença
Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais informações.

Contato
Autor: Andrey Souza Albano
Email: andreysouzaalbano@gmail.com
GitHub: https://github.com/AtisPolac