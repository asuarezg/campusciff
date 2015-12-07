# Ejercicios 
## Ejercicios Git

__1. Crear repositorio campusciff__:

__2. Clonar repositorio en local__

```
# Creamos carpeta en local y conectamos con repositorio remoto.
   mkdir campusciff
   cd campusciff
   git init
   git remote add origin git@github.com:asuarezg/campusciff.git
```

__3. Crear en local documento README__
```
# Traemos archivo Readme.md de repositorio remoto
   git pull origin master
```

__4.Modificar README y hacer Commit Inicial__
```
   git add .
   git commit -m "Commit Inicial"
# Subimos los cambios al repositorio GitHub
   git push origin master
```
__5.Ignorar Archivos__
```
# Creamos carpeta y archivo a ignorar
   touch privado.txt
   mkdir privada
# Configuramos Git para que ignore
   echo privado.txt > .gitignore
   echo privada >> .gitignore
```
__6.Añadir archivo al repositorio local__
```
   touch 1.txt
   git add .
# Verificamos que los archivos ingnorados no están marcados para subir
   git status
# Hacemos commit de los cambios a subir
   git commit -m "Añadido fichero 1.txt y .gitignore"
```
__7.Crear etiqueta v1.0 y subir cambios__
```
   git tag v0.1
   git push --tag origin master
# Si nos equivocamos, podemos borrar la etiqueta
#  git tag -d <nombre-etiqueta-a-borrar>
```
__8.Crear rama v0.2, posicionarse en ella, crear fichero y subir cambios__
```
   git branch v0.2
   git checkout v0.2
# Comprobamos que estamos posicionados
   git list
# Creamos fichero
   touch 2.txt
   git add .
   git commit -m "añadido 2.txt y modificado readme"
   git push origin v0.2
```
__9.Hacer merge directo de rama v0.2 con rama master__
```
   git checkout master 
   git merge v0.2 -m "merge con la rama v0.2"
```
__10.Hacer merge provocando conflicto__
```
# Modificamos fichero 1.txt en rama Master
   echo "Hola" > 1.txt
   git add . 
   git commit -m "Modificado fichero 1.txt"
# Modificamos fichero 1.txt en rama v0.2
   git checkout v0.2
   echo "Adios" > 1.txt
   git add . 
   git commit -m "Modificado en v0.2 fichero 1.txt"   
# Volvemos a rama master y hacemos merge
   git checkout master 
   git merge v0.2 -m "merge con conflicto con la rama v0.2"
# Listamos ramas con merge (la master) y sin merge (la v0.2)
   git branch --merged
   git branch --no-merged
# Resolvemos conflicto y hacemos commit
   VI 1.txt
   git add .
   git commit -m "resuelto conflicto en fichero 1.txt"  
   git push origin master
```
__11.Crear nuevo tag v0.2 y borrar rama v0.2__
```
   git tag v0.2
   git branch -d v0.2  
   git push origin master
# El borrado de la rama no se refleja en el repositorio remoto
# Vemos el  listado de commits y ramas
   git log --oneline --decorate --graph --all
# O con el alias creado
   git list
# Subimos cambios en readme
   git add .
   git commit -m "subimos cambios en readme"   
```
## Ejercicios GitHub