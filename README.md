# Legit

## Objetivo
O objetivo deste projeto é criar parâmetros acompanhar alterações em textos legais utilizando softwares de controle de versão (como o git).

### Exemplo

Retirado do comentario de nathanhammond em https://news.ycombinator.com/item?id=3967921:

> nathanhammond 1593 days ago [-]

> I've dreamed up something like this as well and realistically there isn't anything preventing us from using git to manage our laws. > As a strawman to beat up, here is an example of how it could work:
    git clone legislature/generalstatutes
    s/marijuana/sugar/g
    git commit -am "Turn sugar into a controlled substance."
    git request-pull

    Legislators
    If interested, # git branch bill_12345
    git pull nathanhammond/generalstatutes
    // Continue editing the "Sugar as a controlled substance" bill.

    Spin off to committee (read/write to committee members)
    git clone legislature/generalstatutes
    git checkout bill_12345
    // Continue editing the "Sugar as a controlled substance" bill.
    git commit -am "Committee updates."

    Take a vote for leaving committee.
    If successful, # git request-pull

    General legislature takes a vote.
    If successful, # git merge bill_12345 master --signoff (Legislators that voted for it.)

> Benefits:
> - Encourages broader participation in democracy.
> - Cryptographically signed. We'll know if you voted for or wrote it.
> - Tracks history of all changes (at least at the commit level). If something comes out of committee very different from how it went in you can easily find every change.
> - Makes it easier for newspeople to identify how the law is changing.
> - An interface like GitHub over top of the repository could hide all of the complexity, allow for line-by-line comments, and general comments.
> - Registering to the interface with your voter ID could allow for representatives to identify or poll constituents.

## O problema

Os textos legais (constituição, leis, resoluções, etc...) estão em constante mudança. Nem sempre há um controle da versão vigente. 

## A solução

Utilizar git para controlar alterações em leis.

## A origem do conceito

Veja o TED talk
https://www.youtube.com/watch?v=CEN4XNth61o

