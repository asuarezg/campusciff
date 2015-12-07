# Ejercicios Git

__1. Crear repositorio campusciff__

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
__6.Añadir archivo al repositorio local
```
   touch 1.txt
   git add .
# Verificamos que los archivos ingnorados no están marcados para subir
   git status
# Hacemos commit de los cambios a subir
   git commit -m "Añadido fichero 1.txt y .gitignore"
```
__7.Crear etiqueta v1.0 y subir cambios
```
   git tag v0.1
   git push --tag origin master
# Si nos equivocamos, podemos borrar la etiqueta
#  git tag -d <nombre-etiqueta-a-borrar>
```
__8.Crear rama v0.2, posicionarse en ella, crear fichero y subir cambios
```
   git branch v0.2
   git checkout v0.2
# Comprobamos que estamos posicionados
   git list
# Creamos fichero
   touch 2.txt
   git add .
   git commit -m "añadido 2.txt y modificado readme"
```