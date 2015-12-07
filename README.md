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