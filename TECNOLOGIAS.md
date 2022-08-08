# TÉCNOLOGIAS QUE SERÃO UTILIZADAS NO PROJETO

### Versionamento de código
- GitHub

### DevOPS 
- Docker
    * (Justificativa) Utilizaremos para a implementação de cada bloco do projeto (Tópicos abaixo) manténdo a consistência do desenvolvimento entre os programadores.
- GitHub Actions
    * (Justificativa) Integração do Actions com o Docker SWARM para o desenvolvimento de pipelines, automatizando o fluxo de deploy.

### FrontEnd
- [LINGUAGEM DE PROGRAMAÇÃO] TypeScript
    * (Justificativa) Visando manter a consistência do código estabelecendo a tipagem dos dados e padrões de desenvolvimento.
- [FRAMEWORK] Vue.js 3 
    * (Justificativa) Visando uma curva de aprendizado menor para a adaptação de novos desenvolvedores com o professo de desenvolvimento sem perder a escalabilidade.
- [STORE] Pinia
    * (Justificativa) Biblioteca de gerenciamento de estados por contexto mais moderna que Vuex, contendo uma forma de implmentação mais abstraida e direta. 
- [CSS] TailwindCSS
    * (Justificativa) Biblioteca de classes utilitárias CSS para permitir rápido desenvolvimento de interfaces sem comprometer a liberdade de criação de componentes customizados.
- [TESTES] Jest
    (Justificativa) Biblioteca para realizar testes unitários FrontEnd para componentes e store.

### BackEnd
- [LINGUAGEM DE PRPGRAMAÇÃO] Python
    * (Justificativa) Possui curva de aprendizagem mais baixa contendo ótimas soluções para o desenvolvimento de APIs.
- [FRAMEWORK] FastAPI
    * (Justificativa) Moderno para a implementações de APIs REST, possui implementações nativas do framework para envio de arquivos, templates entre outros.
- [ORM] SQLAlchemy
    * (Justificativa) Módulo de ORM utilizado mundialmente para interação com bancos de dados relacionais e NoSQL.
- [VERSIONAMENTO DE BANCO DE DADOS] Alembic
    * (Justificativa) Módulo que permite criar "branches" e "versões" do banco de dados, refletindo a implmentação e descrição do SQLAlchemy.

### Banco de dados
- [MODELO] Relacional SQL
- [SGBD] MySQL
    (Justificativa) Um dos mais famosos e consolidados no mercado. Portanto, pela necessidade de criar grandes relacionamentos entre as tabelas, concluímos que um SGBD de arquitetura relacional fosse a melhor opção.

### Segurança
- JWT para authenticação de sessão dos usuários.
- Criptografia SHA256 dos dados sensíveis que exigem a necessidade de serem salvos no banco de dados.
- Certificação do protocolo HTTPS.
