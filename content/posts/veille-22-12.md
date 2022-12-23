---
title: "Veille de Décembre"
date: 2022-12-24
draft: false
summary: "Quoi de neuf en décembre 2022 sur la toile ?"
tags: [Veille, Dev]
---

## Que s'est-il passé dans le monde du web ce mois ci ? 

### PHP

 * Un article nous rappelant comment bien écrire un controlleur (ou le refactorer). C'est du Laravel, mais ça s'applique clairement à toutes les technos.
    {{< articlelink href="https://medium.com/@macielthiago/laravel-your-controllers-should-look-like-this-c09ff9f40841" title="Laravel — Your controllers should look like this" >}}
 * PHP 8.2 est release, au programme : `readonly classes`, `constant` dans les `Traits`, `null, false, true` en type stand-alone, ...
    {{< articlelink href="https://www.php.net/releases/8.2/en.php" title="PHP 8.2 Release Announcement" >}}
 * Comment (et un peu pourquoi) se servir des `enums` quand on le peut.
    {{< articlelink href="https://thisismehrab.medium.com/best-practice-of-using-php-enums-9c4296ee8426" title="Best practice of using PHP Enums!" >}}

### JS / TS

 * Electron 22.0 est sorti. Ce sera la dernière version compatible avec Windows < 10.
    {{< articlelink href="https://www.electronjs.org/blog/electron-22-0" title="Electron 22.0.0">}}
 * Une librairie qui permet de créer ses `query`, `mutation`, `subscription` GraphQL de façon plutôt simple.

Exemple :
```js
import * as gql from 'gql-query-builder'

const query = gql.query({
  operation: 'thought',
  variables: { id: 1 },
  fields: ['id', 'name', 'thought']
})

console.log(query)

// Output
query ($id: Int) {
  thought (id: $id) {
    id, name, thought
  }
}

// Variables
{ "id": 1 }
```
{{< articlelink href="https://github.com/atulmy/gql-query-builder" title="GraphQL Query Builder" link="Voir le repo Github">}}

### CSS

 * Quand on fait un peu de front, on est toujours confronté aux `media queries`. Cet article rentre dans le détail des possibilités et d'une bonne façon de les mettre en place.
   {{< articlelink href="https://stackdiary.com/css-media-queries/" title="A Practical Guide to CSS Media Queries">}}


### Autres

 * En ce moment, on a pas mal de sujets autour de la communication entre nos services, et donc pas mal de lectures sur les différents protocoles.
Ici, un article plutôt complet sur `gRPC` vs `GraphQL`. Comme souvent, la conclusion est : ça dépend de l'usage. Mais il est toujours intéressant d'aller dans le détails des technologies.
 {{< articlelink href="https://stackoverflow.blog/2022/11/28/when-to-use-grpc-vs-graphql/" title="When to use gRPC vs GraphQL" >}}
 * Vous aimez les Regex ? Moi j'adore ça. Voici un petit guide qui saura ravir les néophites comme les expérimentés !
   {{< articlelink href="https://www.thecodingdev.com/2022/11/the-ultimate-guide-for-regular.html" title=" The Ultimate Guide for Regular Expressions (Regex) " >}}
* C'est décembre, alors le truc à ne pas manquer c'était le {{< newtabref href="https://adventofcode.com/" title="Advent of Code" >}} !
