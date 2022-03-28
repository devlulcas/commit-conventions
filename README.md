# 📏 CONVENÇÃO DE COMMITS

> As mensagens de commit devem seguir uma estrutura padronizada para melhorar a semântica do histórico do repositório.

```
tipo(escopo): mensagem
```

## Recomendações:

- **Procure commitar suas alterações de forma frequente. Evite acumular muitas alterações pois isso pode levar a confusão e dificuldade no momento de decidir que tipo de commit deve ser escrito na mensagem.**

- **Quando commitar, procure sempre selecionar as alterações com o menor número de dependências (`imports`) possíveis.**

## Tipos padrões:

### **<build:>**

- Build: Use esse tipo para indicar que sua mudança altera o nosso esquema de build. Isso pode acontecer quando você muda uma configuração do vite, typescript ou npm, por exemplo.

> Exemplo de uso:

```bash
git commit -m "build: mudança do base path do vite"
```

### **<deps:>**

- Dependências: Use esse tipo para indicar que sua mudança altera ou adiciona uma dependência.

> Exemplo de uso:

```bash
git commit -m "deps: react atualizado"
```

### **<remove:>**

- Remover: Use esse tipo para indicar que você removeu um arquivo do projeto

> Exemplo de uso:

```bash
git commit -m "remove: gitkeep"
```

### **<style:>**

- Estilo: Trata de mudanças no estilo do código e não do estilo da aplicação. Formatar código, remover espaços em branco, adicionar ou remover linhas em branco, etc.

> Exemplo de uso:

```bash
git commit -m "style: remoção de linhas em branco"
```

### **<feat:>**

- Funcionalidade: Use esse tipo para indicar que está adicionando uma nova funcionalidade. Pode ser uma outra rota, um novo componente ou até mesmo um novo jeito de usar um filtro, por exemplo.
- Corresponde a uma _minor version_ (0.x.0)

> Exemplo de uso:

```bash
git commit -m "feat: opções de visualização de gráficos"
```

### **<refactor:>**

- Refatoração: Uma mudança de código que nem adiciona uma funcionalidade e nem arruma um bug. Pode ser utilizado quando trocamos os nomes das variáveis de um método para algo mais semântico, por exemplo.

> Exemplo de uso:

```bash
git commit -m "refactor: melhora nos nomes de variáveis e funções"
```

### **<perf:>**

- Performance: Usado em casos onde a mudança tem como objetivo melhorar a performance da aplicação.

> Exemplo de uso:

```bash
git commit -m "perf: redução da quantidade de requests feitas a cada minuto"
```

### **<todo:>**

- Para fazer: Use este tipo quando adicionar apenas uma anotação de coisas para fazer.

> Exemplo de uso:

```ts
// TODO: componente para selecionar região geográfica
```

```bash
git commit -m "todo: componente de seleção de região"
```

### **<docs:>**

- Você deve usar esse tipo quando adicionar algo nas documentações.
- Use o escopo `(dev)` quando a adição for na documentação de desenvolvimento
- Use o escopo `(user)` quando a adição for na documentação de usuários
- Use o escopo `(code)` quando a adição for na documentação de código feita com comentários dentro dos arquivos em src

> Exemplo de uso:

```bash
git commit -m "docs(dev): instruções para conexão com a API"
```

```bash
git commit -m "docs(user): como usar os filtros de data"
```

```bash
git commit -m "docs(code): uso da tipagem no stateType"
```

### **<revert:>**

- Você deve usar esse tipo quando for voltar na linha do tempo do repositório.

> Exemplo de uso:

```bash
git commit -m "revert: voltando para quando meu código ainda funcionava"
```

### **<fix:>**

- Você deve usar o tipo `fix` quando for corrigir algum bug ou erro no código.
- Corresponde a uma _patch version_ (0.0.x)
- Quando a correção se tratar de um erro de ortografia use o escopo `(typo)`

> Exemplos de uso:

```bash
git commit -m "fix: problema com cors"
```

```bash
git commit -m "fix(typo): você escrito como vossê"
```
