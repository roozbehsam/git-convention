# git-convention

convention for git messages

    
## messages:
 
```
    <type> - <module> (<scope>): <subject>
    <BLANK LINE>
    <body>
    <BLANK LINE>
    <footer>
```
_example:_
```
    fix - admin(middleware): ensure Range headers adhere more closely to RFC 2616

    Add one new dependency, use `range-parser` (Express dependency) to compute
    range. It is more well-tested in the wild.

    Fixes #2310
```

 
+ **Type** describes the kind of change that this commit is providing.   
    - **feat** (feature)
    - **fix** (bug fix)
    - **docs** (documentation)
    - **style** (formatting, missing semicolons, …)
    - **refactor**
    - **test** (when adding missing tests)
    - **perf** (performance improvement)
    - **chore** (for updating build configuration, development tools or other changes irrelevant to the user)
+ **Scope**   
    _example:_
    - forms
    - router
    - login
    - admin log
- **Subject** is a very short description of the change, in   
    - imperative, present tense: “change” not             
        “changed”/“changes”
    - no capitalised first letter
    - no dot (.) at the end
- **Body** should include the motivation for the change and      
contrast this with previous behavior and must be phrased in   
imperative present tense 
- **Footer** should contain any information about Breaking       
Changes and is also the place to reference GitHub issues that   
    this commit closes
