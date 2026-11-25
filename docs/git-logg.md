# Git-logg

Klistra in utskrifter och svara på frågorna. Det här är din dokumentation av dagens arbete.

## 1. Utgångsläget

Skriv ut `git log --oneline --graph --all` direkt efter att du klonat. Klistra in här:

```


git log --oneline --graph --all

* 5a5841d (HEAD -> main, origin/main, origin/HEAD) Modul 5 i TypeScript med Vite
* 3804533 Add files via upload
* f7a13a4 Add files via upload
* c9a0075 Initial commit
```

## 2. Merge utan konflikt

Klistra in `git log --oneline --graph --all` efter merge:

```
git log --oneline --graph --all

*   77887ff (HEAD -> main) Merge branch 'meny-nyheter'
|\
| * 6274dd5 (meny-nyheter) Add Tea with milk to the menu
* | b64bb2d kontakt.md Task 3 - Added phone number
|/
* 5a5841d (origin/main, origin/HEAD) Modul 5 i TypeScript med Vite
* 3804533 Add files via upload
* f7a13a4 Add files via upload
* c9a0075 Initial commit
```

Fråga: Vad är skillnaden mellan en _fast-forward_-merge och en merge som skapar en egen merge-commit? Svara med egna ord:
fast-forward : means the main doesnt have any new commits since we created the new branch which makes git moves the pointer without a merge commit
while
merge commit is needed when there are commits in each branch that the other doesnt have so git create this merge commit to combine history of both branches

## 3. Konflikten

Klistra in filen med konfliktmarkörerna, precis som den såg ut innan du löste den:

```

Vardagar: 07–18
<<<<<<< HEAD
Helger: 10–17
=======
Helger: 09–18
>>>>>>> oppettider-sommar
Röda dagar: stängt
```

Fråga: Vad betyder `<<<<<<< HEAD`, `=======` och `>>>>>>> grennamn`?
<<<<<<< HEAD`    : means the next lines are lines in current branch that have conflict`>>>>>>> grennamn : means the lines above it are comming from branch asking for merge
======= : means a separator between the two versions

Hur löste du den, och varför blev det så?
i chossed to have a new line

## 4. Ångra

Vad är skillnaden mellan `git restore`, `git revert` och `git reset`? Vilken är säkrast när ändringen redan är pushad?

`git restore` : works locally to undo changes that have been made but not commited
`git revert` : work on commits by creating another commit that reverting it
`git reset` : changes the head of the branch by moving it backword which could affect other people using same branch

## 5. Pull request

Länk till din pull request (på ditt eget repo):

https://github.com/Marihan89/marihan-m5-dag09-git-grenar/pull/1

## 6. Reflektion

Vad är det värsta som kan hända om man kör `git push --force` på en gren som andra använder?
