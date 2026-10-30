# Practica GIT

## Introducción
```bash
mkdir prueba_git
cd prueba_git

Adrian G@DESKTOP-KB9PHSP MINGW64 ~/prueba_git

nano texto.txt
nano script.sh
nano texto.txt
nano script.bat

$ chmod a+x script.sh
$ ./script.sh
```
```
Resultado consola:
Listado completo
total 3
-rw-r--r-- 1 Adrian G 197121 29 Oct 14 11:08 script.bat
-rw-r--r-- 1 Adrian G 197121 28 Oct 14 11:12 script.sh
-rw-r--r-- 1 Adrian G 197121 13 Oct 14 11:05 texto.txt
```
## Ejercicio1
```bash
1. $ git init

2. $ git status

3. $ git branch -m main

4. $ git branch -m master

```
```text
Resultado consola:
1. Initialized empty Git repository in C:/Users/Adrian G/prueba_git/.git/

2. On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        script.bat
        script.sh
        texto.txt

nothing added to commit but untracked files present (use "git add" to
track)


3. Adrian G@DESKTOP-KB9PHSP MINGW64 ~/prueba_git (main)

4. Adrian G@DESKTOP-KB9PHSP MINGW64 ~/prueba_git (master)
```
## Ejercicio2
```bash
1. $ git add script.bat

2. $ git status

3. $ git commit -m "Confirmacion inicial"

4. $ git status

5. $ git add texto.txt

6. $ git commit -m "Añadido archivo texto.txt"

7. $ git status



```

```text
1. warning: in the working copy of 'script.bat', LF will b
e replaced by CRLF the next time Git touches it

2. On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   script.bat
        new file:   script.sh

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        texto.txt

 3. $ git commit -m "Confirmacion inicial"
[master (root-commit) 2369b2f] Confirmacion inicial
 2 files changed, 4 insertions(+)
 create mode 100644 script.bat
 create mode 100644 script.sh


 4. $ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        texto.txt

nothing added to commit but untracked files present (use "git add" to track)

 
  5. warning: in the working copy of 'texto.txt', LF will be replaced by
 CRLF the next time Git touches it

  6. [master b255e25] Añadido archivo texto.txt
 1 file changed, 3 insertions(+)
 create mode 100644 texto.txt

  7. On branch master
nothing to commit, working tree clean
```
## Ejercicio3
```bash
1. $ git status

2. $ git add texto.txt

3. $ git status

4. $ git commit -m "Ampliada la explicacion del texto"

5. $ git status


```
```text
1. On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   texto.txt

no changes added to commit (use "git add" and/or "git commit -a")

2. warning: in the working copy of 'texto.txt', LF will be replaced by CRLF the next time Git touches it.

3.On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   texto.txt

4. 
[master 1905066] Ampliada la explicacion del texto
 1 file changed, 1 insertion(+), 1 deletion(-)
        
5. On branch master
nothing to commit, working tree clean

```
## Ejercicio4

```bash
1. $ git commit -a -m “Nueva versión”

2. $ git show

3. $ git log

```
```text
1. On branch master
nothing to commit, working tree clean

2. commit 19050663277eac1881e8d288c0d5878ee9d36644 (HEAD -> master)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:05:27 2026 +0100

    Ampliada la explicacion del texto

diff --git a/texto.txt b/texto.txt
index 15bf608..8a5999e 100644
--- a/texto.txt
+++ b/texto.txt
@@ -1,3 +1,3 @@
-uno
+1SXuno
 dos
 tres


3. commit 19050663277eac1881e8d288c0d5878ee9d36644 (HEAD -> master)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:05:27 2026 +0100

    Ampliada la explicacion del texto

commit b255e25db21d31620b9b27e9ccec0c0e6fbb908b
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 16 13:54:43 2026 +0200

    Añadido archivo texto.txt

commit 2369b2f34b02792565f6876d513fb7cec4a304fc
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 16 13:43:30 2026 +0200

    Confirmacion inicial


```

## Ejercicio5
```bash 
1. $ nano texto.txt

2. $ git diff

3. $ git commit -a -m "Probando diff"

4. $ nano texto.txt

5. $ git diff

```

```text
2. warning: in the working copy of 'texto.txt', LF will be replaced by CRLF the next time Git touches it
diff --git a/texto.txt b/texto.txt
index 8a5999e..2ba3072 100644
--- a/texto.txt
+++ b/texto.txt
@@ -1,3 +1,5 @@
-1SXuno
-dos
+uno
+do
 tres
+
+dkt


3. warning: in the working copy of 'texto.txt', LF will be replaced by CRLF the next time Git touches i
t
[master 6852175] Probando diff
 1 file changed, 4 insertions(+), 2 deletions(-)


5. warning: in the working copy of 'texto.txt', LF will be replaced by CRLF the next time Git touches it
diff --git a/texto.txt b/texto.txt
index 2ba3072..afc47a8 100644
--- a/texto.txt
+++ b/texto.txt
@@ -3,3 +3,5 @@ do
 tres

 dkt
+
+hola
```
## Ejercicio6
```bash 
1. $ nano texto.txt

2. $ ls -a

3. $ git status

4. $ git add .

5. $ git commit -m “Añadidos fuentes en java y archivos importantes”

6. $ git ls-tree --name-only -r HEAD
```
```text

2. ./   .git/      importante~       script.bat  temporal~
../  Hola.java  punto6.gitignore  script.sh   texto.txt

3. On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   texto.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Hola.java
        importante~
        punto6.gitignore
        temporal~

no changes added to commit (use "git add" and/or "git commit -a")

4. warning: in the working copy of 'texto.txt', LF will be replaced by CRLF the next time Git touches it

5. [master e9e7825] Añadidos fuents en java y archivos importantes
 5 files changed, 14 insertions(+)
 create mode 100644 Hola.java
 create mode 100644 importante~
 create mode 100644 punto6.gitignore
 create mode 100644 temporal~

 6. Hola.java
importante~
punto6.gitignore
script.bat
script.sh
temporal~
texto.txt
```
## Ejercicio7
```bash 
1. $ git show 685217546bd9a5e1e24c4d5bd9929feb3936e258

2. $ git tag v0.7

3. $ git tag v0.3 685217546bd9a5e1e24c4d5bd9929feb3936e258

4. $ git log --oneline

5. $ git show v0.3

6. $ git checkout v0.3

7. $ git checkout master


```
```text
1. 
commit 685217546bd9a5e1e24c4d5bd9929feb3936e258
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:14:03 2026 +0100

    Probando diff

diff --git a/texto.txt b/texto.txt
index 8a5999e..2ba3072 100644
--- a/texto.txt
+++ b/texto.txt
@@ -1,3 +1,5 @@
-1SXuno
-dos
+uno
+do
 tres
+
+dkt

4. 
e9e7825 (HEAD -> master, tag: v0.7) Añadidos fuents en java y archivos importantes
6852175 (tag: v0.3) Probando diff
1905066 Ampliada la explicacion del texto
b255e25 Añadido archivo texto.txt
2369b2f Confirmacion inicial

5. 
commit 685217546bd9a5e1e24c4d5bd9929feb3936e258 (tag: v0.3)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:14:03 2026 +0100

    Probando diff

diff --git a/texto.txt b/texto.txt
index 8a5999e..2ba3072 100644
--- a/texto.txt
+++ b/texto.txt
@@ -1,3 +1,5 @@
-1SXuno
-dos
+uno
+do
 tres
+
+dkt

6. 
Note: switching to 'v0.3'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6852175 Probando diff

7. 
Previous HEAD position was 6852175 Probando diff
Switched to branch 'master'

```
## Ejercicio8
```bash 
1. $ git branch Prueba

2. $ git log --oneline

3. $ git branch

4. $ git switch Prueba

5. $ git branch

6. $ git log --oneline

7. $ git commit -a -m "Rama para pruebas de código"

8. $ git log --oneline

9. $ git commit -a -m “Llegan los Ents a Java”

10. $ git tag v0.7-Ent-Release

11. $ git log

12. $ cat Hola.java

13. $ git merge Prueba

```

```text
2.
e9e7825 (HEAD -> master, tag: v0.7, Prueba) Añadidos fuents en java y archivos importantes
6852175 (tag: v0.3) Probando diff
1905066 Ampliada la explicacion del texto
b255e25 Añadido archivo texto.txt
2369b2f Confirmacion inicial

3. 
  Prueba
* master

4.
Switched to branch 'Prueba'

5.
* Prueba
  master

6.
e9e7825 (HEAD -> Prueba, tag: v0.7, master) Añadidos fuents en java y archivos importantes
6852175 (tag: v0.3) Probando diff
1905066 Ampliada la explicacion del texto
b255e25 Añadido archivo texto.txt
2369b2f Confirmacion inicial

7. 
On branch Prueba
nothing to commit, working tree clean

8. 
e9e7825 (HEAD -> Prueba, tag: v0.7, master) Añadidos fuents en java y archivos importantes
6852175 (tag: v0.3) Probando diff
1905066 Ampliada la explicacion del texto
b255e25 Añadido archivo texto.txt
2369b2f Confirmacion inicial

9. 
[Prueba b751f84] Llegan los Ents a Java
 1 file changed, 1 insertion(+)


11.
commit b751f84af6d3c09b1fecd57a990d66626063d057 (HEAD -> Prueba, tag: v0.7-Ent-Release)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:40:56 2026 +0100

    Llegan los Ents a Java

commit e9e782581d49a768a1a30115f46e125ebf56512d (tag: v0.7, master)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:24:12 2026 +0100

    Añadidos fuents en java y archivos importantes

commit 685217546bd9a5e1e24c4d5bd9929feb3936e258 (tag: v0.3)
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:14:03 2026 +0100

    Probando diff

commit 19050663277eac1881e8d288c0d5878ee9d36644
Author: AdrianG <xadrigb21@gmail.com>
Date:   Fri Oct 30 10:05:27 2026 +0100

    Ampliada la explicacion del texto

commit b255e25db21d31620b9b27e9ccec0c0e6fbb908b
Author: AdrianG <xadrigb21@gmail.com> 

12.
class Hola {
 public static void main(String[] args){
 System.out.println("Welcome to the Java World");
 }
}

13.
Updating e9e7825..b751f84
Fast-forward
 Hola.java | 1 +
 1 file changed, 1 insertion(+)

```
## Ejercicio 9

```bash 
1. $ git rm importante~

2. $ git commit -a -m "Hola"

3. $ git reset HEAD *.class
```
```text
1.
rm 'importante~'

2.
[master 3ed1926] Hola
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 importante~

```

## Ejercicio 10

```bash
1. $ git remote add origin https://github.com/addrigmz/Practica-Git

2. $ git branch -M main

3. $ git pull

4. $ git push -u origin main

5. $ git push -u origin Prueba


```

```text
3. 
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 862 bytes | 95.00 KiB/s, done.
From https://github.com/addrigmz/Practica-Git
 * [new branch]      main       -> origin/main
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


4.
Enumerating objects: 27, done.
Counting objects: 100% (27/27), done.
Delta compression using up to 6 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (26/26), 2.28 KiB | 466.00 KiB/s, done.
Total 26 (delta 8), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (8/8), done.
To https://github.com/addrigmz/Practica-Git
   57ebece..9ed6220  main -> main
branch 'main' set up to track 'origin/main'.

5.
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'Prueba' on GitHub by visiting:
remote:      https://github.com/addrigmz/Practica-Git/pull/new/Prueba
remote:
To https://github.com/addrigmz/Practica-Git
 * [new branch]      Prueba -> Prueba
branch 'Prueba' set up to track 'origin/Prueba'.

```
