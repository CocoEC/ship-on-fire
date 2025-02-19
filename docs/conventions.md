# Conventions à respecter pour ce projet

* Écrire en anglais dans tout ce qui est code source et commits
* Formater votre code : utilisez par exemple l'extension clangd pour VS Code, avec un fichier de configuration (`.clang-format`) présent à la racine du projet, contenant :
```yaml
BasedOnStyle: LLVM
AllowShortFunctionsOnASingleLine: None
IndentWidth: 4
UseTab: Never
```
* Commenter précisément ce que fait chaque fonction que vous écrivez, mais sans être redondant, *cf* [ce post SO](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/). Utilisez l'impératif dans ces commentaires :
```c
// return foo computation
int foo(int input) {...}
```
* git :
    - Un commit ne doit pas contenir des modifications en lien avec des éléments qui n'ont rien à voir ; préférez faire plusieurs commits séparés.
    - Formater les noms des commits en s'inspirant de [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) :
    ```
    feat: implement data struct X
    fix(backend): remove memory leak in function Y
    
    Vous pouvez aussi utiliser les préfixes suivants : 
    build:, chore:, ci:, docs:, style:, refactor:, perf:, test:
    ```
    - Ne pousser que du code qui compile.
    - Travailler sur des fonctionnalités distinctes dans des branches séparées, et faire des pull request.