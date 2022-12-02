## Convention de commits Git
Documentation offcielle
https://www.conventionalcommits.org/en/v1.0.0/

Documentation Angular :
https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional

Est complémentaire à l'utilisation de [[Versionning| SemVer]] qui défini une convention de versioning 

Exemple : 

```
fix(api): prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```

Exemple 2 :
```
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

Mot clé issue d'[[Angular]]
-   **build**: Changes that affect the build system or external dependencies
- chore: tout le reste
-   **ci**: Changes to our CI configuration files and scripts 
-   **docs**: Documentation only changes
-   **feat**: A new feature
-   **fix**: A bug fix
-   **perf**: A code change that improves performance
-   **refactor**: A code change that neither fixes a bug nor adds a feature
-   **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
-   **test**: Adding missing tests or correcting existing tests


