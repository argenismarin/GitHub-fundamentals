# Fundamentos

## Configuración inicial

### Configuración de usuario
Para establecer el nombre y correo del usuario:

```bash
git config --global user.name "Argenis Marin"
git config --global user.email "armarina@unal.edu.co"
```

### Configuración del editor
Para configurar Visual Studio Code como editor por defecto (espera a que se cierre el editor para confirmar los cambios):

```bash
git config --global core.editor "code --wait"
```

### Configuración de colores
Para habilitar los colores en la salida de Git:

```bash
git config --global color.ui true
```

### Configuración de saltos de línea

- **Windows**: Para que los saltos de línea sean compatibles:

```bash
git config --global core.autocrlf true
```

- **Linux**: Para que Git no modifique automáticamente los saltos de línea:

```bash
git config --global core.autocrlf input
```

## Primeros pasos

### Inicializar un repositorio
Para iniciar un repositorio:

```bash
git init
```

### Área de preparación
Para agregar un archivo al área de preparación:

```bash
git add archivo.txt
```

Para agregar varios archivos, sepáralos con espacios:

```bash
git add archivo.txt otroarchivo.txt
```

Para remover un archivo del área de preparación:

```bash
git rm --cached archivo.txt
```

### Consultar el estado
Para consultar el estado del repositorio:

```bash
git status
```

### Realizar commits
Para realizar un commit con un comentario corto:

```bash
git commit -m "Comentario para subir"
```

Para realizar un commit con un comentario largo en el editor de código:

```bash
git commit
```

Para omitir el área de preparación y realizar el commit directamente:

```bash
git commit -a
```

## Restore, Checkout y más

### Recuperar archivos
Para recuperar un archivo que se eliminó:

```bash
git restore archivo.txt
```

Para devolver un archivo al estado anterior tras un commit:

```bash
git checkout archivo.txt
```

### Modificar nombres de archivos
Para renombrar un archivo:

```bash
git mv prueba1.txt archivo2.txt
```

### Mejorar el estado
Para obtener un estado más limpio y ordenado:

```bash
git status --short
```

## GIT DIFF

### Mostrar contenido
Para mostrar el contenido que ya está en el commit:

```bash
git show archivo.txt
```

### Comparar diferencias
Para mostrar la diferencia entre dos archivos (compara el commit con el staged):

```bash
git diff --staged
```

Para comparar diferencia entre commits por el log en versión corta:

```bash
git log --oneline
```

Para cambiar el número de hash (codificación) del commit:

```bash
git config --global core.abbrev 8
```

Para comparar entre dos commits:

```bash
git diff hash1 hash2
```

Para solo saber los archivos que cambiaron:

```bash
git diff --name-only
```

Para mirar exactamente las líneas que cambiaron:

```bash
git diff --word-diff hash1 hash2
```

## Modificar y deshacer commits

### Modificar commits
Para modificar commits:

```bash
git commit --amend
```

## Ramas diferentes

### Ver y manejar ramas
Para ver las ramas:

```bash
git branch
```

Para crear ramas:

```bash
git branch rama-nombre
```

Para cambiar a otra rama:

```bash
git switch rama-nombre
```

Para crear y cambiar de rama:

```bash
git switch -c rama-nombre2
```

### Borrar y renombrar ramas
Para borrar una rama:

```bash
git branch -d rama-nombre2
```

Para cambiar el nombre de una rama:

```bash
git branch -m rama-nombre2 rama-nombre3
```

Para cambiar el nombre de la rama actual:

```bash
git branch -m nombre-nuevo
```

## Merge

### Unificar ramas
Para unificar una rama a la original:

```bash
git merge rama-mejorada
```

### Revertir cambios
Para devolverme usar:

```bash
git reset --hard commitnuevo
```

## Clonar repositorios

Para descargarlo en la computador

git clone enlace

Para llevar a la plataforma desde mi pc

