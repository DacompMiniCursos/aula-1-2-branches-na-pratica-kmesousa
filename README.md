# sobre o projeto
O projeto é uma simulação do uso de branches, tratando de sua criação, merge e resolução de conflitos. Foram documentados o histório e tragetória do projeto, disponíveis abaixo.

**simulação do conflito de branches: features do projeto**
Sobre.txt: arquivo de texto que discorrerá sobre minha tragetória no git
Contatos.py: dicionário com contatos no qual o usuário poderá adicionar novos contatos

# histórico e evolução do projeto

## log final
```
*   c2d3dd9 (HEAD -> main) Merge branch 'feature/contatos'
|\  
| * 15f3b28 (feature/contatos) implementanto contatos.py e descrição no sobre o projeto do readme
* | 85e2f0d (feature/sobre) adicionando sobre.txt e descrições da branch
|/  
* 75a20a8 iniciando o repositório e rasucnho do readme
```

## entry #01
- não percebi o erro de ortografica em 'rascunho'


**git log**
```
* 75a20a8 (HEAD -> main) iniciando o repositório e rasucnho do readme
```

## entry #02
criação da branch feat/sobre \
propositalmente deixei de fora no commit que foram feitas alterações no readme

**git diff**
```
diff --git a/README.md b/README.md
index b70c2b6..a987912 100644
--- a/README.md
+++ b/README.md
@@ -1,4 +1,5 @@
 # sobre o projeto
+Eu fiquei responsável pela branch feature sobre e decidi que esse projeto vai conter um arquivo txt sobre.txt detalhado que discorrerá sobre minha tragetória no git
```

**git log**
```
* 85e2f0d (HEAD -> feature/sobre) adicionando sobre.txt e descrições da branch
* 75a20a8 (main) iniciando o repositório e rasucnho do readme
```

## entry #03
criação da branch featue/contatos \
commit foi mais detalhado e mencionou que foram feitas alterações no sobre do readme, porém, faço uma simulação de se tratar de outro desenvolvedor, que não sabe que também foram feitas alterações no mesmo local em outra branch

**git diff**
```
diff --git a/README.md b/README.md
index b70c2b6..6480763 100644
--- a/README.md
+++ b/README.md
@@ -1,4 +1,5 @@
 # sobre o projeto
+Contatos.py: dicionário com contatos no qual o usuário poderá adicionar novos contatos

diff --git a/contatos.py b/contatos.py
new file mode 100644
```

**git log**
```
* 15f3b28 (HEAD -> feature/contatos) implementanto contatos.py e descrição no sobre o projeto do readme
| * 85e2f0d (feature/sobre) adicionando sobre.txt e descrições da branch
|/  
* 75a20a8 (main) iniciando o repositório e rasucnho do readme
```

## entry #04
merge das branches no main

### 4.1 merge da branch feature/sobre

```
git merge feature/sobre
Updating 75a20a8..85e2f0d
Fast-forward
 README.md | 1 +
 sobre.txt | 6 ++++++
 2 files changed, 7 insertions(+)
 create mode 100644 sobre.txt
 ```

### 4.2 merge da branch feature/contatos

```
 git merge feature/contatos
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result

```

**conflito no readme:**
```
<<<<<< HEAD
Eu fiquei responsável pela branch feature sobre e decidi que esse projeto vai conter um arquivo txt sobre.txt detalhado que discorrerá sobre minha tragetória no git
=======
Contatos.py: dicionário com contatos no qual o usuário poderá adicionar novos contatos
>>>>>> feature/contatos
'''
```

**solução do conflito:**
```
**features do projeto usadas como simulação do conflito de branches**
Sobre.txt: arquivo de texto que discorrerá sobre minha tragetória no git
Contatos.py: dicionário com contatos no qual o usuário poderá adicionar novos contatos
```

**git log**
```
*   c2d3dd9 (HEAD -> main) Merge branch 'feature/contatos'
|\  
| * 15f3b28 (feature/contatos) implementanto contatos.py e descrição no sobre o projeto do readme
* | 85e2f0d (feature/sobre) adicionando sobre.txt e descrições da branch
|/  
* 75a20a8 iniciando o repositório e rasucnho do readme
```

## entry #05
edição e organização do readme

**git diff**
```
diff --git a/README.md b/README.md
index 8bbeebf..86e0f3b 100644
--- a/README.md
+++ b/README.md
@@ -1,6 +1,7 @@
 # sobre o projeto
+O projeto é uma simulação do uso de branches, tratando de sua criação, merge e resolução de conflitos. Foram documentados o histório e tragetória do projeto, disponíveis abaixo.
 
-**features do projeto usadas como simulação do conflito de branches**
+**simulação do conflito de branches: features do projeto**
 Sobre.txt: arquivo de texto que discorrerá sobre minha tragetória no git
```

**git log** \
vai criar um paradoxo deixa quieto