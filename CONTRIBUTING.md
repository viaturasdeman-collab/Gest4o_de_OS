# CONTRIBUTING

Bem-vindo! Este documento descreve como contribuir para o projeto Gest4o de OS.

## 🚀 Como Começar uma Nova Tarefa

### Tipos de Tarefa
- 🐛 **Bug/Correção** - Reportar e corrigir problemas
- ✨ **Enhancement/Melhoria** - Melhorias em features existentes
- 🎉 **Feature/Nova Função** - Novas funcionalidades

### Processo
1. **Criar Issue** descrevendo a tarefa com clareza
2. **Atribuir a si mesmo** (assignee)
3. **Adicionar labels** apropriadas (priority, type, area)
4. **Associar a um milestone** (release planejada)
5. **Implementar localmente** em uma branch dedicada
6. **Abrir PR** referenciando a Issue

---

## 📝 Padrão de Commits

Utilizamos **Conventional Commits** para manter histórico limpo:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- `feat`: Nova funcionalidade
- `fix`: Correção de bug
- `docs`: Documentação
- `style`: Formatação/estilo (sem lógica)
- `refactor`: Refatoração (sem alterações externas)
- `perf`: Melhoria de performance
- `test`: Adicionar/alterar testes
- `chore`: Dependências, configurações

### Exemplos
```
feat(csv): adicionar suporte para importação de CSV

fix(ui): corrigir animação de skeleton no mobile

test: aumentar cobertura de utils para 85%

docs: atualizar README com instruções de setup
```

---

## 🔄 Fluxo de Pull Request

### 1. Criar Branch
```bash
# Feature nova
git checkout -b feat/descricao-curta

# Correção
git checkout -b fix/numero-issue
```

### 2. Implementar Changes
- ✅ Seguir linting rules: `npm run lint:fix`
- ✅ Escrever testes para novas funcionalidades
- ✅ Manter coverage acima de 80%: `npm run test:coverage`
- ✅ Testes E2E passando: `npm run test:e2e`
- ✅ Validar commits: `npm run lint:commits`

### 3. Abrir PR
- Usar **template de PR** fornecido
- **Referenciar Issue**: `Closes #123` ou `Fixes #456`
- Descrever mudanças e motivação
- Incluir screenshots se alterações UI
- Adicionar labels relevantes

**Template Padrão:**
```markdown
## Descrição
Breve descrição do que foi mudado e por quê.

## Issues Relacionadas
Closes #123

## Tipo de Mudança
- [ ] Bug fix
- [ ] Feature nova
- [ ] Breaking change
- [ ] Documentation

## Checklist
- [ ] Linting passou (`npm run lint`)
- [ ] Testes unitários passaram (`npm run test`)
- [ ] Coverage mantido > 80%
- [ ] Testes E2E passaram
- [ ] Commits seguem Conventional Commits
- [ ] PR referencia Issue

## Screenshots (se aplicável)
```

### 4. Code Review
- ✓ Revisor valida lógica e qualidade
- ✓ Verificar testes passando
- ✓ Verificar linting limpo
- ✓ Discussão construtiva de mudanças

### 5. Merge
- Squash commits se múltiplos
- Deletar branch após merge

---

## 🏷️ Labels Padrão

### Priority
- 🔴 `priority:critical` - Bloqueia release/produção
- 🟠 `priority:high` - Importante, próximo sprint
- 🟡 `priority:medium` - Normal, planejado
- 🟢 `priority:low` - Nice-to-have, quando houver tempo

### Type
- `type:bug` - Correção de problema
- `type:enhancement` - Melhoria em feature existente
- `type:feature` - Nova funcionalidade
- `type:documentation` - Apenas docs
- `type:refactor` - Reorganização sem lógica nova

### Status
- `status:in-progress` - Em desenvolvimento
- `status:review` - Aguardando revisão
- `status:blocked` - Bloqueado por outra tarefa
- `status:ready` - Pronto para fazer

### Area
- `area:ui` - Interface/UX
- `area:backend` - Lógica/API
- `area:devops` - Infraestrutura/CI-CD
- `area:tests` - Testes
- `area:docs` - Documentação

---

## 🛠️ Checklist para Implementação

Antes de abrir um PR, verifique:

- [ ] Código segue linting rules: `npm run lint:fix`
- [ ] Testes unitários adicionados: `npm run test`
- [ ] Cobertura mantida > 80%: `npm run test:coverage`
- [ ] Testes E2E passando: `npm run test:e2e`
- [ ] CONTRIBUTING.md atualizado (se necessário)
- [ ] Commit messages seguem Conventional Commits
- [ ] PR referencia Issue com `Closes #XXX`
- [ ] Branch é atualizado com `main`: `git pull origin main`
- [ ] Sem conflitos para merge

---

## 🏗️ Stack Técnico

| Aspecto | Tecnologia |
|---------|-----------|
| **Linguagem** | JavaScript (HTML/CSS/JS puro) |
| **Build Tool** | Não aplicável (HTML estático) |
| **Testing (Unit)** | Vitest |
| **Testing (E2E)** | Playwright |
| **Linting** | Biome (ESLint + Prettier) |
| **Commits** | CommitLint + Conventional Commits |
| **CI/CD** | GitHub Actions |
| **Deployment** | GitHub Pages |

---

## 🔍 Observabilidade & Qualidade

| Ferramenta | Propósito |
|-----------|----------|
| **Sentry** | Error tracking e monitoring |
| **Datadog** | Performance monitoring (RUM) |
| **OpenTelemetry** | Distributed tracing |
| **Codecov** | Coverage reporting |
| **Arch-contract** | Validação de arquitetura |
| **Knip** | Dependências não utilizadas |
| **Stryke** | Mutation testing |

---

## 📋 Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev              # Inicia servidor local

# Qualidade
npm run lint             # Verifica linting
npm run lint:fix         # Corrige automaticamente

# Testes
npm run test             # Testes unitários
npm run test:ui          # UI interativa de testes
npm run test:coverage    # Cobertura de testes
npm run test:e2e         # Testes end-to-end

# Verificações
npm run arch             # Valida arquitetura
npm run knip             # Encontra deps não usadas
npm run test:mutations   # Mutation testing

# Build
npm run build            # Build para produção
```

---

## 🤝 Código de Conduta

- ✅ Seja respeitoso com outros contribuidores
- ✅ Forneça feedback construtivo
- ✅ Aceite críticas construtivas com graça
- ✅ Foque no que é melhor para a comunidade
- ✅ Demonstre empatia com outros membros

---

## 📞 Perguntas & Discussões

- 💬 **Dúvidas sobre contribute?** Abra uma Discussion
- 🐛 **Encontrou um bug?** Abra uma Issue com o label `type:bug`
- 💡 **Sugestão de feature?** Abra uma Issue com o label `type:feature`
- 🎯 **Quer ajudar?** Procure por issues com label `good first issue` ou `help wanted`

---

## 🚀 Roadmap de Qualidade

Estamos trabalhando em:

1. **✅ GitHub Workflow** - Templates de Issues e PRs
2. **✅ Motion Design** - Skeleton screens e animações
3. **✅ Linting** - Biome, CommitLint, Arch-contract
4. **✅ Testes Unit/Integration** - Vitest com codecov
5. **✅ Testes E2E** - Playwright
6. **✅ Observabilidade** - Sentry, Datadog, OpenTelemetry

---

## 📚 Referências Úteis

- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [Vitest Documentation](https://vitest.dev/)
- [Playwright Documentation](https://playwright.dev/)
- [Biome Documentation](https://biomejs.dev/)

---

**Obrigado por contribuir! 🎉**

Aprecia-se cada contribuição, grande ou pequena.
