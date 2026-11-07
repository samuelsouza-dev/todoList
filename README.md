# Lista de Tarefas

Aplicação web de tarefas e lembretes escrita em TypeScript, usando classes e interfaces.

## Funcionalidades

- **Tarefas:** adiciona uma tarefa com descrição e a exibe na lista.
- **Troca de modo:** o botão **Toggle Mode** alterna entre os formulários de tarefa e de lembrete.
- **Lembretes:** o formulário pede descrição, data e canal de notificação (SMS, e-mail ou push), mas ainda não funciona. Veja as [limitações](#limitações-conhecidas).

## Tecnologias

- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="20" alt=""> TypeScript
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="20" alt=""> HTML

## Como executar

Clone o repositório:

```bash
git clone https://github.com/samuelsouza-dev/todoList.git
```

O JavaScript compilado já está no repositório, então basta abrir `public/index.html` no navegador.

### Para alterar o código

É necessário ter o Node.js instalado. Entre na pasta do projeto:

```bash
cd todoList
```

Instale as dependências:

```bash
npm install
```

Inicie a compilação:

```bash
npm run build
```

O comando fica em execução e recompila `src/index.ts` para `public/dist/index.js` a cada alteração. Para encerrar, pressione `Ctrl+C`.

## Estrutura do projeto

```text
├── public/
│   ├── index.html      # Interface
│   └── dist/index.js   # Código compilado
├── src/index.ts        # Código-fonte
├── package.json
└── tsconfig.json
```

## Limitações conhecidas

- **Lembretes não são criados:** o código procura os campos `notifications` e `reminderDate`, mas o HTML os chama de `notification` e `scheduleDate`. Ao enviar o formulário, ocorre um erro no console.
- **Sem persistência:** as tarefas ficam em memória e são perdidas ao recarregar a página.
- **Sem edição:** não é possível concluir nem remover uma tarefa pela interface.
- **Sem notificações:** nenhum código envia SMS, e-mail ou push. O canal escolhido seria apenas exibido na lista.

## Licença

Distribuído sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).
