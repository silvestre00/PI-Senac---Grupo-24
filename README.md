# Modelagem de um Sistema Orientado a Objetos
> Senac EAD - Projeto Integrador.
#### Integrantes:
- #### Silvestre Alves de Almeida Neto
- #### Vinicius da Silva Ferreira
- #### Emile de Sousa Moraes Tavares
- #### Charles Mamor Iwamoto Filho
- #### Fernanda Mayara Severino

## Descrição:
  Apresentamos a seguir **Diagrama de Caso de uso** e **Diagrama de Classe** de um projeto de um sistema voltado a gestão de dados de uma grande universidade. Apresentando alguns casos de uso com tópicos principais e alternativos para cada tipo de cadastro a ser realizado no sistema da universidade. Além disto apresentamos também um prototipo funcional utilizando figma para facilitar o entendimento do nosso projeto.

## Cenários de caso de uso:
- Cadastro de Pessoa Física.
- Cadastro de Pessoa Jurídica.
- Cadastro de Professores.
- Cadastro de Fornecedores.
- Cadastro de Alunos.
> ## Cada tópico esta organizado da seguinte forma.
> - Cenário Principal.
> - Cenário Alternativo 1.
> - Cenário Alternativo 2.

### Prototipo Figma:
  https://www.figma.com/proto/5hxqtEGhppE0FuL8vjPmak/Senac-prototipo?node-id=121-133&node-type=canvas&t=z3B74dMzKuJq6T7V-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1
### Aqui esta a __classe principal__ para ajudar no entendimento das demais e do conteúdo deste repositório.

> ## Pessoa.
>Var   | Type
>--------- | ------
>id | intenger
>nome | varchar
>dataNascimento | date/time
>ativo | varchar
>endereco | id_endereco
>telefone | id_telefone

https://github.com/user-attachments/assets/7b951706-1d06-4ca1-93e7-20f93b2f5b74

# Cenários de Caso de Uso

## 1. Cadastro de Pessoa Física

### Cenário Principal
1. O usuário acessa o sistema e seleciona a opção **"Cadastro de Pessoa Física"**.
2. O sistema solicita informações como nome, CPF, endereço, telefone e dados de nascimento.
3. O usuário preenche os dados obrigatórios e confirma o cadastro.
4. O sistema valida os dados e salva as informações na base de dados.
5. O sistema exibe uma mensagem de sucesso indicando que a pessoa foi cadastrada com sucesso.

### Cenário Alternativo 1
- O usuário tenta cadastrar uma pessoa física cujo CPF já está registrado no sistema.
  - O sistema exibe uma mensagem de erro informando que o CPF já existe.
  - O usuário deve corrigir os dados ou atualizar o cadastro existente.

### Cenário Alternativo 2
- O usuário deixa de preencher um campo obrigatório (como CPF ou nome).
  - O sistema detecta o campo vazio e exibe uma mensagem solicitando o preenchimento do campo.
  - O usuário preenche o campo faltante e tenta novamente salvar o cadastro.

### Pré-condição
- O usuário deve estar autenticado no sistema e ter permissão para realizar cadastros.

### Pós-condição
- A nova pessoa física é cadastrada no sistema, com todos os dados obrigatórios preenchidos e validados.

---

## 2. Cadastro de Pessoa Jurídica

### Cenário Principal
1. O usuário acessa o sistema e seleciona a opção **"Cadastro de Pessoa Jurídica"**.
2. O sistema solicita informações como razão social, CNPJ, endereço e telefone.
3. O usuário preenche os dados e confirma o cadastro.
4. O sistema valida as informações, incluindo o CNPJ.
5. O sistema salva as informações na base de dados e exibe uma mensagem de sucesso.

### Cenário Alternativo 1
- O usuário tenta cadastrar uma pessoa jurídica cujo CNPJ já está registrado no sistema.
  - O sistema exibe uma mensagem de erro indicando que o CNPJ já existe.
  - O usuário pode revisar o cadastro existente ou tentar corrigir os dados.

### Cenário Alternativo 2
- O sistema não consegue validar o CNPJ (CNPJ inválido ou incorreto).
  - O sistema exibe uma mensagem de erro informando que o CNPJ fornecido é inválido.
  - O usuário pode revisar e corrigir o CNPJ antes de tentar novamente.

### Pré-condição
- O usuário deve ter permissão para cadastrar novas pessoas jurídicas.

### Pós-condição
- A pessoa jurídica é cadastrada com sucesso no sistema e suas informações estão disponíveis para futuras interações.

---

## 3. Cadastro de Professores

### Cenário Principal
1. O usuário acessa o sistema e seleciona a opção **"Cadastro de Professores"**.
2. O sistema solicita dados como nome, CPF, departamento, salário e informações de contato.
3. O usuário preenche os campos e confirma o cadastro.
4. O sistema valida as informações e salva os dados do professor na base de dados.
5. O sistema exibe uma mensagem de sucesso indicando que o professor foi cadastrado corretamente.

### Cenário Alternativo 1
- O usuário tenta cadastrar um professor com CPF já existente no sistema.
  - O sistema exibe uma mensagem de erro informando que o CPF já está cadastrado.
  - O usuário pode revisar o cadastro ou atualizar as informações.

### Cenário Alternativo 2
- O usuário deixa de preencher o campo do departamento.
  - O sistema alerta sobre o campo obrigatório e solicita o preenchimento.
  - O usuário corrige o erro e tenta salvar novamente.

### Pré-condição
- O sistema deve estar configurado para registrar professores e o usuário deve ter acesso a essa funcionalidade.

### Pós-condição
- O professor é cadastrado com sucesso no sistema, com todas as informações validadas.

---

## 4. Cadastro de Fornecedores

### Cenário Principal
1. O usuário acessa o sistema e seleciona a opção **"Cadastro de Fornecedores"**.
2. O sistema solicita informações como razão social, CNPJ, produto fornecido e contato.
3. O usuário preenche os dados e confirma o cadastro.
4. O sistema valida as informações e salva os dados do fornecedor.
5. O sistema exibe uma mensagem de sucesso confirmando o cadastro.

### Cenário Alternativo 1
- O usuário tenta cadastrar um fornecedor com CNPJ já existente.
  - O sistema exibe uma mensagem de erro, informando que o CNPJ já está cadastrado.
  - O usuário pode revisar os dados ou atualizar o cadastro.

### Cenário Alternativo 2
- O usuário deixa de preencher o campo do produto fornecido.
  - O sistema alerta sobre o campo obrigatório e solicita correção.
  - O usuário corrige o erro e submete o cadastro novamente.

### Pré-condição
- O usuário deve ter permissão para cadastrar fornecedores no sistema.

### Pós-condição
- O fornecedor é cadastrado e está disponível para interações no sistema.

---

## 5. Cadastro de Alunos

### Cenário Principal
1. O usuário acessa o sistema e seleciona a opção **"Cadastro de Alunos"**.
2. O sistema solicita informações como nome, CPF, matrícula, curso e telefone.
3. O usuário preenche os dados e confirma o cadastro.
4. O sistema valida as informações e salva os dados do aluno.
5. O sistema exibe uma mensagem confirmando o sucesso do cadastro.

### Cenário Alternativo 1
- O usuário tenta cadastrar um aluno com CPF ou matrícula já existente no sistema.
  - O sistema exibe uma mensagem de erro, informando duplicidade de dados.
  - O usuário pode corrigir ou atualizar o cadastro.

### Cenário Alternativo 2
- O usuário esquece de preencher a matrícula do aluno.
  - O sistema alerta sobre o campo obrigatório e solicita que o dado seja inserido.
  - O usuário corrige o campo e tenta novamente.

### Pré-condição
- O usuário deve ter permissão para realizar cadastros de alunos.

### Pós-condição
- O aluno é cadastrado corretamente no sistema, com todos os dados validados.

---

Essas descrições detalham os cenários para os casos de uso solicitados, cobrindo tanto o fluxo principal quanto os alternativos, assim como as pré-condições e pós-condições para garantir a consistência no sistema.

