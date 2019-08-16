# Regras <!-- omit in toc -->

- [Mensagens de Commit](#mensagens-de-commit)
  - [Exemplos sem corpo](#exemplos-sem-corpo)
  - [Exemplos com corpo](#exemplos-com-corpo)
- [Conteúdo](#conte%c3%bado)
- [Recomendações Adicionais](#recomenda%c3%a7%c3%b5es-adicionais)

## Mensagens de Commit

1. **Título deve ter até 72 caracteres**
    - Facilita para ver histórico no console, ex.: `git log --oneline`
    - Há ferramentas que cortam (truncam) mensagens em 72 caracteres ao exibir
    - Se puder, mantenha em 50 caracteres
2. **Título deve começar com letra maiúscula**
    - Padroniza e facilita pesquisa
3. **Título deve começar com um verbo, conjugado na terceira pessoa do singular**
    - Padroniza e vai direto ao ponto
4. **Título não deve usar voz passiva**
    - Melhora compreensão e padroniza estilo
5. **Título não deve terminar com ponto final**
    - Títulos não tem ponto final
6. **Título deve ser separado do corpo da mensagem por uma linha vazia**
    - Esse é um padrão em ferramentas de controle de versão, como o Git
7. **Corpo é opcional**
    - Muitas vezes o título basta
8. **Corpo deve explicar *o que* e *porquê*, não *como***
    - Foco na contribuição

### Exemplos sem corpo

- `Adiciona exportação para PDF`
- `Refatora a classe Foo`
- `Remove os arquivos foo.json e bar.xml`
- `Conclui a tarefa #123`
- `Documenta o componente Xpto`
- `Aceita o merge #456`
- `Aceita o merge #456 de usuario/algum-branch`
- `Atualiza a versão para 1.2.1`
- `Corrige #123 sobre a rebimboca da parafuseta`

### Exemplos com corpo
```
Desfaz "Adiciona exportação para PDF"

Reverte o commit c83d7a9ac83d7a9ac83d7a9ac83d7a9ac83d7a9a
```

```
Libera versão 1.3.0

Novidades:
- Nova rosqueta da parafuseta, veja #125
- Melhoria de desempenho na arruela da grapeta
- Correção de #123 na rebimboca da parafuseta
- Correção de #124 na mola da grampola
```

## Conteúdo

1. **Sempre submeta um conjunto de arquivos que participaram de uma *única* atividade**
    - Permite desfazer commits sem afetar outras atividades
    - Facilita rastrear modificações em arquivos pela mensagem de commit

2. **Separe commits com correções dos commits com alterações**
    - Permite desfazer commits sem afetar outras atividades
    - Facilita a aplicação de um commit com correções em outros branches

3. **Não submeta código que não compila**
    - Verifique a compilação/interpretação antes de submeter

4. **Integre todos os dias**
    - Evita acumular coisas a integrar
    - Dê `fetch` em seu *branch* todos os dias, para obter atualizações de outros da equipe
    - Dê `merge` de *branches* estáveis para o *seu* (*e.g.*, `master`), para obter atualizações de outros

5. **Reserve um tempo diário para integração**
    - Ajuda a cumprir a Regra 4
    - Facilita a organização do seu trabalho

6. **Não integre quando estiver no meio de uma tarefa**
    - Facilita a integração

7. **Atualize antes de submeter**
    - Dê `fetch` (ou `pull`) antes de dar `push`
    - Faça `merge` com um *branch* antes de enviar um `merge request`
        - por exemplo, se você está trabalhando em `branch-123` e mais tarde vai fazer um `merge request` para o branch `master`, você deve obter as atualizações de `master` antes de fazer o `merge request`. Isso evitará dores de cabeça na integração


## Recomendações Adicionais

1. **Crie *branches* diferentes para tarefas e correções**
    - Auxilia a separação das atividades - veja Regras 1 e 2

2. **Organize-se para realizar uma coisa de cada vez**
    - Cumprir regras como 1, 2, 5 e 6 requer organização. Procure planejar suas atividades antes de começar.

3. **Submeta trabalho incompleto para branches remotos pessoais**
    - Se no fim do dia, você não conseguiu terminar uma tarefa, submeta-a para um *branch* remoto pessoal. Assim, você reduz o risco de perder seu trabalho caso seu computador local dê problema, garante que outros tenham acesso em caso de necessidade e não interfere no trabalho de ninguém.

4. **Submeta trabalho incompleto para o *stash* ao integrar**
    - Use `stash` apropriadamente, para não perder seu trabalho ou para facilitar a integração.

5. **Use ferramentas para detectar problemas antes de commitar**
   - Configure *hooks* que ocorram antes de um *commit* ou de um *push*
   - Use *linters* para detectar problemas ou possíveis falhas.
   - Verifique se seu código compila corretamente.
   - Verifique se seu código passa nos testes automatizados.


[Voltar](readme.md)
