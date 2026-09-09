# 🚀 Guia Desenvolvimento e Fluxo do Git

Este repositório utiliza o modelo de desenvolvimento baseado em **Feature Branches** e integração contínua via **Pull Requests (PRs)**. 

Para garantir a estabilidade do sistema, **a branch `main` é protegida**: nenhum desenvolvedor pode fazer commits diretamente nela. Todas as alterações devem ser enviadas por meio de uma nova branch e revisadas por um dos administradores do projeto.

---

## 👥 Papéis e Permissões do Time

* **Administradores (Anna e Guilherme):** Responsáveis por revisar, aprovar e integrar (merge) os Pull Requests, além de manter a estabilidade da branch `main`.
* **Desenvolvedores (Emanuel, João Marcelo e Ryan):** Responsáveis por criar branches secundárias, implementar funcionalidades/correções e abrir Pull Requests para revisão.

---

## 💻 Passo a Passo para Desenvolvedores

Siga este procedimento para cada nova funcionalidade, correção ou alteração que for realizar no projeto:

### 1. Atualize sua `main` local
Sempre comece garantindo que seu código local possui as últimas alterações do projeto:
```bash
git checkout main
git pull origin main
```

### 2. Crie uma nova branch para a sua tarefa
Crie uma branch secundária para isolar o seu trabalho. Use um nome descritivo com letras minúsculas e hífen:
```bash
git checkout -b feature/nome-da-sua-tarefa
```
*(Certifique-se de que o terminal indica que você mudou para a nova branch antes de editar qualquer arquivo)*.

### 3. Desenvolva e registre suas alterações
Trabalhe normalmente no seu editor de código. Ao concluir uma etapa da tarefa:
```bash
git add .
git commit -m "feat: descricao sucinta do que foi feito"
```

### 4. Envie sua branch para o GitHub
```bash
git push origin feature/nome-da-sua-tarefa
```

### 5. Abra um Pull Request (PR)
1. Acesse o repositório do projeto no GitHub.
2. Clique no aviso amarelo **Compare & pull request** na página inicial.
3. Preencha o Título e a Descrição usando o **Modelo de PR** (disponível abaixo neste documento).
4. No menu lateral direito (**Reviewers**), marque **um dos administradores**.
5. Clique em **Create pull request**.

### 6. Acompanhe a revisão
* Se o código for aprovado, o administrador integrará as alterações à branch `main`.
* Caso sejam solicitados ajustes, faça as alterações necessárias no seu computador, salve e rode:
  ```bash
  git add .
  git commit -m "fix: ajusta alteracoes solicitadas"
  git push origin feature/nome-da-sua-tarefa
  ```
  *(O Pull Request no GitHub será atualizado automaticamente com o novo commit)*.

---

## 📋 Modelo (Template) para Descrição de Pull Requests

Copie e cole a estrutura abaixo no campo de descrição ao abrir um novo PR no GitHub:

### 📌 Descrição
- [Breve resumo do que foi implementado ou corrigido nesta tarefa]

### 🧪 O que foi feito?
- [ ] Item 1 (ex: Criada a interface da tela de login)
- [ ] Item 2 (ex: Adicionada validação dos campos de email e senha)
- [ ] Item 3 (ex: Integrado com a API de autenticação)

### 🔍 Como testar?
1. Faça o checkout para a branch deste PR.
2. Execute o projeto localmente.
3. Acesse a tela ou funcionalidade alterada e valide os cenários.

---

## 💡 Padronização de Commits e Boas Práticas

Utilize prefixos padrão no início de cada mensagem de commit para organizar o histórico do projeto:

* `feat:` Novas funcionalidades (ex: `feat: adiciona componente de menu`).
* `fix:` Correção de erros ou bugs (ex: `fix: corrige alinhamento no mobile`).
* `docs:` Alterações em documentações ou arquivos README (ex: `docs: atualiza instrucoes de instalacao`).
* `style:` Formatação de código ou ajustes visuais que não alteram a lógica (ex: `style: ajusta espacamento do CSS`).

Para mais, esse reposítório mostra os padrões e suas descrições: [Padrões de Commits](https://github.com/iuricode/padroes-de-commits).
---

## 🚨 Regras Importantes
* **Nunca** faça commits diretos na `main`.
* **Nunca** force um envio (`git push --force`) sem orientação prévia dos administradores.
* Caso surja algum problema de conflito de código (merge conflict), peça ajuda a um dos administradores antes de prosseguir.
