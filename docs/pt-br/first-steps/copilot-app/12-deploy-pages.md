---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um workflow do Pages, revisar o pull request e verificar se o Space Quiz está no ar."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz com o GitHub Pages para disponibilizá-lo ao público. O Copilot pode preparar o workflow e orientar a publicação, mas você continua responsável por revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma implantação no GitHub Pages.
- revisar o workflow e o pull request antes da mesclagem.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages disponibiliza uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site se necessário e o publique no GitHub Pages. Adicione um README que descreva o aplicativo e como executá-lo localmente, caso ainda não exista. Crie um pull request com essas mudanças e faça a mesclagem depois que as verificações obrigatórias forem aprovadas. Monitore a implantação até que ela seja concluída com sucesso e, em seguida, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou mesclar, diga exatamente o que preciso aprovar ou fazer; não informe que a tarefa foi concluída até o site estar no ar.
```

![Diagrama em três etapas: pull request do space-quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente para criar e mesclar um pull request e alterar as configurações de Pages do repositório. Antes de prosseguir, revise o diff, as permissões de implantação e quaisquer solicitações de aprovação do GitHub.

## Revise o workflow e verifique a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de compilação e implantação do workflow.
3. Faça a mesclagem somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz está disponível como um site publicado, e você verificou a implantação em vez de confiar no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
